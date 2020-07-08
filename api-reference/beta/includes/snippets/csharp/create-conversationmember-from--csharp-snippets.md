---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: eeed9495ac9e88bcd14d2b6fa1c5c0ad5f3cf441
ms.sourcegitcommit: 2050639c9e9a6b2dab9ce53d6a9fc87e98789b50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/08/2020
ms.locfileid: "45080905"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var conversationMember = new AadUserConversationMember
{
    Roles = new List<String>()
    {
        "owner"
    },
    UserId = "50dffbae-ad0f-428e-a86f-f53b0acfc641",
    DisplayName = "Cameron White",
    Email = "CameronW@M365x987948.OnMicrosoft.com"
};

await graphClient.Teams["{id}"].Members
    .Request()
    .AddAsync(conversationMember);

```