---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: b7583238e24f5fe34739d01d90b2ee0893bd7727
ms.sourcegitcommit: df2c52f84aae5d4fed641d7411ba547371f0eaad
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2020
ms.locfileid: "44055598"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const permission = {
  type: "view",
  password: "ThisIsMyPrivatePassword",
  scope: "anonymous"
};

let res = await client.api('/me/drive/items/{item-id}/createLink')
    .post(permission);

```