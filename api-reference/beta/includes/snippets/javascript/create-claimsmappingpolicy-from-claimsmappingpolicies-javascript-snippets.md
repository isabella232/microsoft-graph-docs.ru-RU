---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 754553d925e325e0c34de415c07139ca6d111371
ms.sourcegitcommit: c4d6ccd343a6b298a2aa844f1bad66c736487251
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/11/2020
ms.locfileid: "42589808"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const claimsMappingPolicy = {
  definition: [
    "definition-value"
  ],
  displayName: "displayName-value",
  isOrganizationDefault: true
};

let res = await client.api('/policies/claimsMappingPolicies')
    .version('beta')
    .post(claimsMappingPolicy);

```