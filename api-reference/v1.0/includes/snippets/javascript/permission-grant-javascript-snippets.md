---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 384d73316cecc45be23d713e057640e70accd809
ms.sourcegitcommit: bd40e302ce04b686e86989246ab7c4cc9ad3f320
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/03/2020
ms.locfileid: "43124884"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const permission = {
  recipients: [
    {
      email: "john@contoso.com"
    },
    {
      email: "ryan@external.com"
    }
  ],
  roles: ["read"]
};

let res = await client.api('/shares/{encoded-sharing-url}/permission/grant')
    .post(permission);

```