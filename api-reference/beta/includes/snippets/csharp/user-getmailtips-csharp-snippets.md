---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: c4fadabb3b5c9bd95bef6475abad4cbdbbd27018
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48608706"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var emailAddresses = new List<String>()
{
    "danas@contoso.onmicrosoft.com",
    "fannyd@contoso.onmicrosoft.com"
};

var mailTipsOptions = MailTipsType.AutomaticReplies | MailTipsType.MailboxFullStatus;

await graphClient.Me
    .GetMailTips(emailAddresses,mailTipsOptions)
    .Request()
    .PostAsync();

```