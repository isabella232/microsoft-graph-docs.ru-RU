---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d4a7dd06921208c8ca060cc2d940a15d3d577617
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48603332"
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
      skuId: "guid"
    }
  ],
  removeLicenses: [ "bea13e0c-3828-4daa-a392-28af7ff61a0f" ]
};

let res = await client.api('/me/assignLicense')
    .post(user);

```