---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 497dc6fe4c5acaa97007c0753cc4214e49cb4c2d
ms.sourcegitcommit: 0329bbcd5f1b09a2a6c5f935a30c4560b6eed492
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "36638382"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const privilegedRoleAssignment = {
  userId: "userId-value",
  roleId: "roleId-value"
};

let res = await client.api('/privilegedRoleAssignments')
    .version('beta')
    .post(privilegedRoleAssignment);

```