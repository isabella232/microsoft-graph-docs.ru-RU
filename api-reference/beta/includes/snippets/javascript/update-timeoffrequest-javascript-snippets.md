---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f2d6d8f0d553c7fad6c2a9cb1f93fb28faca27c3
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40863546"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const timeOffRequests = {
  startDateTime: "datetime-value",
  endDateTime: "datetime-value",
  timeOffReasonId: "timeOffReasonId-value"
};

let res = await client.api('/teams/{id}/schedule/timeOffRequests')
    .version('beta')
    .update(timeOffRequests);

```