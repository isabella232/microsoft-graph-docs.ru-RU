---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 6d4744d976f772eb20c5b931bc6c5f35111c461c
ms.sourcegitcommit: 2f78ac96a9b0462626a242429055ef824590bd3f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2020
ms.locfileid: "41476592"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const claimsMappingPolicies = {
  @odata.id:"https://graph.microsoft.com/beta/policies/claimsMappingPolicies/cd3d9b57-0aee-4f25-8ee3-ac74ef5986a9"
};

let res = await client.api('/servicePrincipals/{id}/claimsMappingPolicies')
    .version('beta')
    .post(claimsMappingPolicies);

```