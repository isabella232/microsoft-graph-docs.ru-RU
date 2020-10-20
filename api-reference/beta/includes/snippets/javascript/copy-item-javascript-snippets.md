---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 2d04f8dd4ae7ff80f5aba0cce83dd668c92c05cc
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48610574"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const driveItem = {
  parentReference: {
    driveId: "6F7D00BF-FC4D-4E62-9769-6AEA81F3A21B",
    id: "DCD0D3AD-8989-4F23-A5A2-2C086050513F"
  },
  name: "contoso plan (copy).txt"
};

let res = await client.api('/me/drive/items/{item-id}/copy')
    .version('beta')
    .post(driveItem);

```