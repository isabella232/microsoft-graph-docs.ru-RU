---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 226045b3eb15a376540eb52e59570d1afdb85fdf
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46570028"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/identityProtection/riskDetections/c2b6c2b9-dddc-acd0-2b39-d519d803dbc3')
    .version('beta')
    .get();

```