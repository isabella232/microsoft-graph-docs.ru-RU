---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 291c603ec1841fad0b25801e80eb1eece7edb886
ms.sourcegitcommit: 1585d55d3e7030b5fd1f7cfd5de8f9fb8202cd56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2019
ms.locfileid: "37429147"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const resultInfo = {
  value: [
    "externalId-value1",
    "externalId-value2"
  ]
};

let res = await client.api('/security/tiIndicators/deleteTiIndicatorsByExternalId')
    .version('beta')
    .post(resultInfo);

```