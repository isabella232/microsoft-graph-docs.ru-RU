---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ea3199cf13b103d25b93ce1403f82b2913454eda
ms.sourcegitcommit: 46ee19b244349e2a1537f0c44c576d7c01cf03a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/05/2019
ms.locfileid: "37402359"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const governanceRoleSetting = {
   adminEligibleSettings:[
      {
         ruleIdentifier:"ExpirationRule",
         setting:{\"permanentAssignment\:false,\maximumGrantPeriodInMinutes\:129600}"
      }
   ]
};

let res = await client.api('/privilegedAccess/azureResources/roleSettings/5fb5aef8-1081-4b8e-bb16-9d5d0385bab5')
    .version('beta')
    .update(governanceRoleSetting);

```