---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: b690c25dd01da7d1ca72a7b7ec44f87fd9c684c3
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35488753"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const plannerBucket = {
  name: "Advertising",
  planId: "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  orderHint: " !"
};

let res = await client.api('/planner/buckets')
    .version('beta')
    .post({plannerBucket : plannerBucket});

```