---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 6aa944b7b598c272020d6e26bb1d6f0ab452eb3d
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48616382"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const user = {
  addLicenses: [
    {
      disabledPlans: [ "11b0131d-43c8-4bbb-b2c8-e80f9a50834a" ],
      skuId: "skuId-value-1"
    },
    {
      disabledPlans: [ "a571ebcc-fqe0-4ca2-8c8c-7a284fd6c235" ],
      skuId: "skuId-value-2"
    }
  ],
  removeLicenses: []
};

let res = await client.api('/me/assignLicense')
    .version('beta')
    .post(user);

```