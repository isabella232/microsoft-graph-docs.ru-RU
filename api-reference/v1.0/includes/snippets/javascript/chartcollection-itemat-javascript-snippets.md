---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 27706f8b2d9b6b2d3142024d7d565bda6ed00f6a
ms.sourcegitcommit: 0329bbcd5f1b09a2a6c5f935a30c4560b6eed492
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "36638574"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const workbookChart = {
  index: 8
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/itemAt')
    .post(workbookChart);

```