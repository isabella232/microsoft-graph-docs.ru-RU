---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: eeb8cd0e3a19e639811352a45f9b44e4a6b59bb9
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48610021"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const forward = {
  comment: "comment-value",
  toRecipients: [
    {
      emailAddress: {
        name: "name-value",
        address: "address-value"
      }
    }
  ]
};

let res = await client.api('/groups/{id}/threads/{id}/posts/{id}/forward')
    .post(forward);

```