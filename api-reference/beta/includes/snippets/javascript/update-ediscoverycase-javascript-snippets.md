---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 87504ac8c2cc000483dab352f5eae132b38680c4
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46566928"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const ediscoveryCase = {
  displayName: "My Case 1 - Renamed",
  description: "Updated description",
  externalId: "Updated externalId"
};

let res = await client.api('/compliance/ediscovery/cases/061b9a92-8926-4bd9-b41d-abf35edc7583')
    .version('beta')
    .update(ediscoveryCase);

```