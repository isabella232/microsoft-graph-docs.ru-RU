---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ac01495e9753a6c380465f505e33a547fb49e9a7
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35515951"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const workbookFormatProtection = {
  locked: true,
  formulaHidden: true
};

let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/format/protection')
    .update({workbookFormatProtection : workbookFormatProtection});

```