---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ee33a8ae3a637157487f18f2e50750eac5e5fbe2
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "37992964"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const accessPackageAssignmentPolicy = {
  accessPackageId: "56ff43fd-6b05-48df-9634-956a777fce6d",
  displayName: "direct",
  description: "direct assignments by administrator",
  isEnabled: true
};

let res = await client.api('/identityGovernance/entitlementManagement/accessPackageAssignmentPolicies')
    .version('beta')
    .post(accessPackageAssignmentPolicy);

```