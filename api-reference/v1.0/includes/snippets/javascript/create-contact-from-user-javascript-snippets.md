---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 05cec4f7392df8912b24802bf553a4b31137bfbe
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35497026"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const contact = {
  givenName: "Pavel",
  surname: "Bansky",
  emailAddresses: [
    {
      address: "pavelb@fabrikam.onmicrosoft.com",
      name: "Pavel Bansky"
    }
  ],
  businessPhones: [
    "+1 732 555 0102"
  ]
};

let res = await client.api('/me/contacts')
    .post({contact : contact});

```