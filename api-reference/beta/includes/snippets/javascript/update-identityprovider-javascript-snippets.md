---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 59e9615a412d0e85154f61a36f955d818e8db971
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46566690"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const identityProvider = {
  clientSecret: "1111111111111"
};

let res = await client.api('/identityProviders/Amazon-OAuth')
    .version('beta')
    .update(identityProvider);

```