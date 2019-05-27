---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 379ed9551fed7231c4cb2d06eb632b87a45bed37
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34480836"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var @event = new Event
{
    Subject = "Let's go for lunch",
    Body = new ItemBody
    {
        ContentType = BodyType.Html,
        Content = "Does late morning work for you?"
    },
    Start = new DateTimeTimeZone
    {
        DateTime = "2017-04-15T12:00:00",
        TimeZone = "Pacific Standard Time"
    },
    End = new DateTimeTimeZone
    {
        DateTime = "2017-04-15T14:00:00",
        TimeZone = "Pacific Standard Time"
    },
    Location = new Location
    {
        DisplayName = "Harry's Bar"
    },
    Attendees = new List<Attendee>()
    {
        new Attendee
        {
            EmailAddress = new EmailAddress
            {
                Address = "samanthab@contoso.onmicrosoft.com",
                Name = "Samantha Booth"
            },
            Type = AttendeeType.Required
        }
    }
};

await graphClient.Me.Events
    .Request()
    .Header("Prefer","outlook.timezone=\"Pacific Standard Time\"")
    .AddAsync(@event);

```