---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: be9c99e5b77edda415f3bdf19561caf9e152e377
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48610709"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var group = new Group
{
    Description = "Self help community for library",
    DisplayName = "Library Assist",
    GroupTypes = new List<String>()
    {
        "Unified"
    },
    MailEnabled = true,
    MailNickname = "library",
    SecurityEnabled = false
};

await graphClient.Groups
    .Request()
    .AddAsync(group);

```