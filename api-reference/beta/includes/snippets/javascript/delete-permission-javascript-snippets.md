---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 3a22207a0c999cab19d39407649cc12fa23f2a9a
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35730528"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/root/items/{item-id}/permissions/{perm-id}')
    .version('beta')
    .delete();

```