---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 948ed19e37dd3dfc2f4d902d017308261ec6f3e4
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35717475"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var subscribedSkus = await graphClient.SubscribedSkus
    .Request()
    .GetAsync();

```