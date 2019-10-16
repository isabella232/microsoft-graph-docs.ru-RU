---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 67f6c9eb2f0060191a5c562e1f4d23d16f82ac95
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2019
ms.locfileid: "37544439"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var conversationMember = new AadConversationMember
{
    Roles = new List<String>()
    {
    },
    AdditionalData = new Dictionary<string, object>()
    {
        {"user@odata.bind","https://graph.microsoft.com/beta/users/8b081ef6-4792-4def-b2c9-c363a1bf41d5"}
    }
};

await graphClient.Teams["{id}"].Channels["{id}"].Members
    .Request()
    .AddAsync(conversationMember);

```