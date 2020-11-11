---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 351184bc9b19da12d04be4de9f645649a9405ff8
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48984057"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Boolean notifyTeam = true;

Calendar startDateTime = CalendarSerializer.deserialize("10/8/2018 12:00:00 AM");

Calendar endDateTime = CalendarSerializer.deserialize("10/15/2018 12:00:00 AM");

graphClient.teams("{teamId}").schedule()
    .share(notifyTeam,startDateTime,endDateTime)
    .buildRequest()
    .post();

```