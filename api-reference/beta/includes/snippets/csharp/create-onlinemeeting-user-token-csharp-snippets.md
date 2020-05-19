---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: e119306bff22949bfe15e4f547d8f4be959b2121
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37995403"
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