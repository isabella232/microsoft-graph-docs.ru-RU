---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: e8fa9d76ae5a5771b402a730d024d15b992e0662
ms.sourcegitcommit: a3fc420a5639c0f4e89af2b602db17392e176802
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2020
ms.locfileid: "48223120"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/external/connections/contosohr/groups/31bea3d537902000')
    .version('beta')
    .delete();

```