---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 08941c265f826331572c64f04d13c0c3cca242e8
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37995406"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var onlineMeeting = new OnlineMeeting
{
    IsBroadcast = false,
    StartDateTime = DateTimeOffset.Parse("2019-09-09T21:33:30.8546353+00:00"),
    EndDateTime = DateTimeOffset.Parse("2019-09-09T22:03:30.8566356+00:00"),
    Subject = "Application Token Meeting",
    Participants = new MeetingParticipants
    {
        Organizer = new MeetingParticipantInfo
        {
            Identity = new IdentitySet
            {
                User = new Identity
                {
                    Id = "550fae72-d251-43ec-868c-373732c2704f"
                }
            }
        }
    }
};

await graphClient.Communications.OnlineMeetings
    .Request()
    .AddAsync(onlineMeeting);

```