---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 09db92478233726613c3cf6a3ee34c6f72aabfca
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "48904694"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/totalRowRange')
    .get();

```