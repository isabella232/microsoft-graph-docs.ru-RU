---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 2823bb99ed2b9342e855c66261b86559a1322c3c
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46566719"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const identityProvider = {
  @odata.type: "microsoft.graph.identityProvider",
  name: "Login with Amazon",
  type: "Amazon",
  clientId: "56433757-cadd-4135-8431-2c9e3fd68ae8",
  clientSecret: "000000000000"
};

let res = await client.api('/identityProviders')
    .version('beta')
    .post(identityProvider);

```