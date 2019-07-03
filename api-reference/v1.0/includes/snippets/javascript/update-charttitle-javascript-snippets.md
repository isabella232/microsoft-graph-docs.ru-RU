---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: c99c2415f67375a1f0a3b0d4701f2ef735c501a4
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496639"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const workbookChartTitle = {
  overlay: true,
  text: "text-value",
  visible: true
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/title')
    .update({workbookChartTitle : workbookChartTitle});

```