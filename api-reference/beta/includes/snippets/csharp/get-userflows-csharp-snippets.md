---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: cbf3e98385eecb5403ef7a24ae925bb6297659da
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "37938601"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var userFlows = await graphClient.Identity.UserFlows
    .Request()
    .GetAsync();

```