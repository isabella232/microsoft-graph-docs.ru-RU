---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 6ef57b2d5d64dc2f4d01d9918fe59bf38609adc7
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48622277"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const apply = {
  fields: [
    {
      key: 99,
      sortOn: "sortOn-value",
      ascending: true,
      color: "color-value",
      dataOption: "dataOption-value",
      icon: {
        set: "set-value",
        index: 99
      }
    }
  ],
  matchCase: true,
  hasHeaders: true,
  orientation: "orientation-value",
  method: "method-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/sort/apply')
    .version('beta')
    .post(apply);

```