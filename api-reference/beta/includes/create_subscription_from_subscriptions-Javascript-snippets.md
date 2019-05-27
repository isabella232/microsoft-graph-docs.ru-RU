---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 59c8334330099357beb862bb586941dd63136f61
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34439507"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const subscription = {
   changeType: "created,updated",
   notificationUrl: "https://webhook.azurewebsites.net/api/send/myNotifyClient",
   resource: "me/mailFolders('Inbox')/messages",
   expirationDateTime:"2016-11-20T18:23:45.9356913Z",
   clientState: "secretClientValue"
};

let res = await client.api('/subscriptions')
    .version('beta')
    .post({subscription : subscription});

```