---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ffc796508ca0abce4a57f0ffcca00757f49d52ca
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35859430"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Event event = new Event();
event.originalStartTimeZone = "originalStartTimeZone-value";
event.originalEndTimeZone = "originalEndTimeZone-value";
ResponseStatus responseStatus = new ResponseStatus();
responseStatus.response = ResponseType.NONE;
responseStatus.time = "2016-10-19T10:37:00Z";
event.responseStatus = responseStatus;
event.recurrence = null;
event.uid = "iCalUId-value";
event.reminderMinutesBeforeStart = 99;
event.isReminderOn = true;

graphClient.me().events("{id}")
    .buildRequest()
    .patch(event);

```