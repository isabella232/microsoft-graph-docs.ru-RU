---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 957b0e8db1a6c2094b3b51b04bd043cee6f15d56
ms.sourcegitcommit: 8e18d7fe3c869b2fd48872365116175d3bdce1b7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2020
ms.locfileid: "46643872"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var templates = await graphClient.ServicePrincipals["{id}"].Synchronization.Templates
    .Request()
    .GetAsync();

```