---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 0877eca0d07ea7ec29a372c41a809629ba2b0845
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46566847"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var group = new Group
{
    Description = "Group assignable to a role",
    DisplayName = "Role assignable group",
    GroupTypes = new List<String>()
    {
        "Unified"
    },
    IsAssignableToRole = true,
    MailEnabled = true,
    SecurityEnabled = true,
    MailNickname = "contosohelpdeskadministrators",
    Visibility = "Private"
};

await graphClient.Groups
    .Request()
    .AddAsync(group);

```