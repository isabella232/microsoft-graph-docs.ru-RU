---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 4cbd36eff78180c67091334fe0b6b737bdb51e44
ms.sourcegitcommit: f50b1feff72182d1e19bfa346304beaf29558b68
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2019
ms.locfileid: "36461542"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/roleManagement/directory/roleDefinitions')
    .version('beta')
    .get();

```