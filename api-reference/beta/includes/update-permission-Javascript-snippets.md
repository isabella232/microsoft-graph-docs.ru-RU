---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 92af74ff7f8105926f631ef71f826c8fe3e4321b
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34461976"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const permission = {
  roles: [ "read" ]
};

let res = await client.api('/me/drive/items/{item-id}/permissions/{perm-id}')
    .version('beta')
    .update({permission : permission});

```