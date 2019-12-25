---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: e119306bff22949bfe15e4f547d8f4be959b2121
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40866348"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var onlineMeeting = new OnlineMeeting
{
    StartDateTime = DateTimeOffset.Parse("2019-07-12T21:30:34.2444915+00:00"),
    EndDateTime = DateTimeOffset.Parse("2019-07-12T22:00:34.2464912+00:00"),
    Subject = "User Token Meeting"
};

await graphClient.Me.OnlineMeetings
    .Request()
    .AddAsync(onlineMeeting);

```