---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 26a22f36d51a70d8c76afe09ec088f914a41a992
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35709963"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const cancel = {
  cancellationMessage: "Your appointment has been successfully cancelled. Please call us again."
};

let res = await client.api('/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/appointments/AAMkADKoAAA=/cancel')
    .version('beta')
    .post(cancel);

```