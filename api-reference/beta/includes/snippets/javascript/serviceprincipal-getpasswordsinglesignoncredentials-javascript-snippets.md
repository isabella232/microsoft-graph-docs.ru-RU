---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: c7e187b421b05c41af8f090b77212200f7037f02
ms.sourcegitcommit: d40d2a9266bd376d713382925323aefab285ed69
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "38747851"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const passwordSingleSignOnCredentialSet = {
  id: "5793aa3b-cca9-4794-679a240f8b58"
};

let res = await client.api('/servicePrincipals/{id}/getPasswordSingleSignOnCredentials')
    .version('beta')
    .post(passwordSingleSignOnCredentialSet);

```