---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: fcb2eb5b2d80604694f7d8321907ade6799f69a2
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34446045"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/auditLogs/signIns/{id}')
    .version('beta')
    .get();

```