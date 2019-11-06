---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: e5797adc4d162ce140b3f8b890f7780be4e460e2
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37996271"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const notification = {
  notification: {
    targetHostName: "targetHostName-value",
    appNotificationId: "appNotificationID-value",
    expirationDateTime: "datetime-value",
    targetPolicy: {
      platformTypes: [
        "platformTypes-value"
        ]
      }, 
    payload: {
      rawContent: "rawContent-value",
      visualContent: {
        title: "title-value",
        body: "body-value"
      }
    },
    displayTimeToLive: 99,
    priority: "priority-value",
    groupName: "groupName-value"
  }
};

let res = await client.api('/me/notifications')
    .version('beta')
    .post(notification);

```