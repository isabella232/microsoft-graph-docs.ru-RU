---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ac7f90a164205d9fd6141bef07058bf1561ba257
ms.sourcegitcommit: 5a1373f2ccd9ee813fc60d42e7ac6b115b5f9f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "44336113"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/oauth2PermissionGrants/{id}')
    .delete();

```