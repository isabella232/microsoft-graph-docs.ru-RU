---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 6117be8188565f4456f717f7010ef38ad9dd1553
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35736668"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const setData = {
  sourceData: "sourceData-value",
  seriesBy: "seriesBy-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/setData')
    .post(setData);

```