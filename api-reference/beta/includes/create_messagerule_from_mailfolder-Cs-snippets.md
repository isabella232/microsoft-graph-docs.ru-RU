---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 0b24cb54ce73dfc8e3cd5779c27b04ca17970380
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34440186"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var messageRule = new MessageRule
{
    DisplayName = "From partner",
    Sequence = 2,
    IsEnabled = true,
    Conditions = new MessageRulePredicates
    {
        SenderContains = new List<String>()
        {
            "adele"
        }
    },
    Actions = new MessageRuleActions
    {
        ForwardTo = new List<Recipient>()
        {
            new Recipient
            {
                EmailAddress = new EmailAddress
                {
                    Name = "Alex Wilbur",
                    Address = "AlexW@contoso.onmicrosoft.com"
                }
            }
        },
        StopProcessingRules = true
    }
};

await graphClient.Me.MailFolders["inbox"].MessageRules
    .Request()
    .AddAsync(messageRule);

```