---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 762dcc1208c7cf5581f00d42701a4f2bee295d16
ms.sourcegitcommit: e20c113409836115f338dcfe3162342ef3bd6a4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "45008732"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const schemaExtension = {
  properties: [
    {
      name:"new-name-value",
      type:"new-type-value"
    },
    {
      name:"additional-name-value",
      type:"additional-type-value"
    }
  ]
};

let res = await client.api('/schemaExtensions/{id}')
    .update(schemaExtension);

```