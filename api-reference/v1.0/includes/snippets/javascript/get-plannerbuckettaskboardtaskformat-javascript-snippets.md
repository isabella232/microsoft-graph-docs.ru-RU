---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d56fc46f2e1e4d8d147ccaa333400002e062980e
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48620879"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/planner/tasks/{task-id}/bucketTaskBoardFormat')
    .get();

```