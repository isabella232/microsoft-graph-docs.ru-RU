---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f104453773b4a595f31720b16b475b9f4cd92481
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35712225"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const event = {
  originalStartTimeZone: "originalStartTimeZone-value",
  originalEndTimeZone: "originalEndTimeZone-value",
  responseStatus: {
    response: "",
    time: "2016-10-19T10:37:00Z"
  },
  recurrence: null,
  uid: "iCalUId-value",
  reminderMinutesBeforeStart: 99,
  isReminderOn: true
};

let res = await client.api('/me/events/{id}')
    .version('beta')
    .update({event : event});

```