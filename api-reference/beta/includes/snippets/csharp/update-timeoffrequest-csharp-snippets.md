---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ad5138afef05821a270b63c62bbf14e112ba04dc
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40863545"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var timeOffRequests = new TimeOffRequest
{
    StartDateTime = DateTimeOffset.Parse("datetime-value"),
    EndDateTime = DateTimeOffset.Parse("datetime-value"),
    TimeOffReasonId = "timeOffReasonId-value"
};

await graphClient.Teams["{id}"].Schedule.TimeOffRequests
    .Request()
    .UpdateAsync(timeOffRequests);

```