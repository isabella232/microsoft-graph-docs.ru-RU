---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 4848e4e37bec12fcf2d556eeee62fabdc31d00e8
ms.sourcegitcommit: 726f20403323be7d267b67c2764ed7c244e02ee1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "47329368"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/termStore/groups/{groupId}')
    .version('beta')
    .get();

```