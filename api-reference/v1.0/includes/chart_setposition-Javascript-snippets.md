---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 7c0c862109d094f2168b23ebda3fb29befceeed7
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34469162"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const setPosition = {
  startCell: "startCell-value",
  endCell: "endCell-value"
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/setPosition')
    .post(setPosition);

```