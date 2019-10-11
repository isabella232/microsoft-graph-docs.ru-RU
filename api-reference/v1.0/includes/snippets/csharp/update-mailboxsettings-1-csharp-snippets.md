---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 20d322afd53fd111206e8237544cded55662705d
ms.sourcegitcommit: 1585d55d3e7030b5fd1f7cfd5de8f9fb8202cd56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2019
ms.locfileid: "37427979"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var mailboxSettings = new MailboxSettings
{
    AdditionalData = new Dictionary<string, object>()
    {
        {"@odata.context","https://graph.microsoft.com/v1.0/$metadata#Me/mailboxSettings"}
    },
    AutomaticRepliesSetting = new AutomaticRepliesSetting
    {
        Status = AutomaticRepliesStatus.Scheduled,
        ScheduledStartDateTime = new DateTimeTimeZone
        {
            DateTime = "2016-03-20T18:00:00",
            TimeZone = "UTC"
        },
        ScheduledEndDateTime = new DateTimeTimeZone
        {
            DateTime = "2016-03-28T18:00:00",
            TimeZone = "UTC"
        }
    }
};

var me = new User();
me.MailboxSettings = mailboxSettings;

await graphClient.Me
    .Request()
    .UpdateAsync(me);

```