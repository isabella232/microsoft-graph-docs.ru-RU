---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: fefa9a5c9a41474db07d64004e237932aedffb2b
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35723789"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const closeSession = {

};

let res = await client.api('/me/drive/items/{id}/workbook/closeSession')
    .version('beta')
    .post(closeSession);

```