---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 75efd5ce52f64fdfc864114a92c50d31d307c5c0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496718"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const workbookWorksheet = {
  position: 99,
  name: "name-value",
  visibility: "visibility-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}')
    .update({workbookWorksheet : workbookWorksheet});

```