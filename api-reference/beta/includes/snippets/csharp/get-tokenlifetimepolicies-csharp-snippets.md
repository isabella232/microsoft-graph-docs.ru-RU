---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 3ef64f13d9022edd0460f133fd323b04600226e5
ms.sourcegitcommit: 2f78ac96a9b0462626a242429055ef824590bd3f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2020
ms.locfileid: "41558931"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var policy = await graphClient.Policies["tokenLifetimePolicies"]
    .Request()
    .GetAsync();

```