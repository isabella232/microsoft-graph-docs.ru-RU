---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: b2606c6b2c437b4473da062e4dae24690d90c2a9
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35723871"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const user = {
  accountEnabled: true,
  displayName: "displayName-value",
  mailNickname: "mailNickname-value",
  userPrincipalName: "upn-value@tenant-value.onmicrosoft.com",
  "passwordProfile" : {
    forceChangePasswordNextSignIn: true,
    password: "password-value"
  }
};

let res = await client.api('/users')
    .version('beta')
    .post({user : user});

```