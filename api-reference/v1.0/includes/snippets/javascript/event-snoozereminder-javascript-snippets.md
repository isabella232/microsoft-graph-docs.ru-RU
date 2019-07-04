---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 5c6c8e14db9c5c49c372ccabf622ef24c5a0c2f7
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35515978"
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