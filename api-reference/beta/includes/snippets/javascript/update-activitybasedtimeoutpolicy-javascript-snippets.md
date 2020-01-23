---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: cde95a1863bc0f6d949d76d9cc0e5a4c8bbda953
ms.sourcegitcommit: 2f78ac96a9b0462626a242429055ef824590bd3f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2020
ms.locfileid: "41475453"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const {id} = {
  definition: [
    "definition-value"
  ],
  displayName: "displayName-value",
  isOrganizationDefault: true,
  type: "type-value"
};

let res = await client.api('/policies/activityBasedTimeoutPolicies/{id}')
    .version('beta')
    .update({id});

```