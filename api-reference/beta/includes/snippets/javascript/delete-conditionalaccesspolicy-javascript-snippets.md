---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f0d1a5dc1471a654a543bcac3206fc66ac35d382
ms.sourcegitcommit: 66a52d2e63cf3447ec50bd28e562d99e7c344814
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2020
ms.locfileid: "43062507"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/identity/conditionalAccess/policies/{id}')
    .version('beta')
    .delete();

```