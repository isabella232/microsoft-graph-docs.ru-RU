---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 5c6c8e14db9c5c49c372ccabf622ef24c5a0c2f7
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34457719"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const snoozeReminder = {
  newReminderTime: {
    dateTime: "dateTime-value",
    timeZone: "timeZone-value"
  }
};

let res = await client.api('/me/events/{id}/snoozeReminder')
    .post(snoozeReminder);

```