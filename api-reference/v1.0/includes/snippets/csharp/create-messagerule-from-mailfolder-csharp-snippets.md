---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 0b24cb54ce73dfc8e3cd5779c27b04ca17970380
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35472783"
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