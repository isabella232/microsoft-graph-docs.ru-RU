---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 589b3b16ea4adbb15d1dda5e354fdfdeff4ffdaa
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48603474"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var messageRule = new MessageRule
{
    DisplayName = "Important from partner",
    Actions = new MessageRuleActions
    {
        MarkImportance = Importance.High
    }
};

await graphClient.Me.MailFolders["inbox"].MessageRules["AQAAAJ5dZqA="]
    .Request()
    .UpdateAsync(messageRule);

```