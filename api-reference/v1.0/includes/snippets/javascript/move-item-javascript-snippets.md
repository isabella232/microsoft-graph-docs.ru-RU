---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: e405405786ff922db56683bfdc117365cde0a7be
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496933"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const driveItem = {
  parentReference: {
    id: "{new-parent-folder-id}"
  },
  name: "new-item-name.txt"
};

let res = await client.api('/me/drive/items/{item-id}')
    .update({driveItem : driveItem});

```