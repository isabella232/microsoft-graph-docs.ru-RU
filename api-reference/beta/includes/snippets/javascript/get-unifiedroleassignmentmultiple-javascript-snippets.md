---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 83d73242de4755af0cd268d2b07b8d59817bd718
ms.sourcegitcommit: 5a1373f2ccd9ee813fc60d42e7ac6b115b5f9f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "44338860"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/roleManagement/deviceManagement/roleAssignments')
    .version('beta')
    .filter(' principalIds/any(x:x eq '564ae70c-73d9-476b-820b-fb61eb7384b9')')
    .get();

```