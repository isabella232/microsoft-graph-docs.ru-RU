---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: bee2dba19933af2228dbac33626e6e8fab8abc0d
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37995402"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const onlineMeeting = {
  startDateTime:"2019-07-12T14:30:34.2444915-07:00",
  endDateTime:"2019-07-12T15:00:34.2464912-07:00",
  subject:"User Token Meeting"
};

let res = await client.api('/me/onlineMeetings')
    .version('beta')
    .post(onlineMeeting);

```