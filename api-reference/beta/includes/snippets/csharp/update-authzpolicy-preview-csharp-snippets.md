---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f3204ef1ca1924424d66c98bcb1fe8e0c4f7e91c
ms.sourcegitcommit: 726f20403323be7d267b67c2764ed7c244e02ee1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "47842864"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var authorizationPolicy = new AuthorizationPolicy
{
    EnabledPreviewFeatures = new List<String>()
    {
        "assignGroupsToRoles"
    }
};

await graphClient.Policies.AuthorizationPolicy["authorizationPolicy"]
    .Request()
    .UpdateAsync(authorizationPolicy);

```