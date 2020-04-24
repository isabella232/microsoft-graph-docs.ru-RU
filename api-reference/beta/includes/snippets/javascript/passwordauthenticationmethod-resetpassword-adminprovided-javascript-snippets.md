---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 36dfef7cfa7f1ca39b826901116f5ed471394b0a
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2020
ms.locfileid: "43805969"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const passwordResetResponse = {
  newPassword: "newPassword-value",
};

let res = await client.api('/users/{id}/authentication/passwordMethods/{id}/resetPassword')
    .version('beta')
    .post(passwordResetResponse);

```