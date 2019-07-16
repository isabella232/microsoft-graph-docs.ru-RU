---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 2c94e56bd1e6b21c7b21c9fea86064c49fded66f
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35740905"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const contactFolder = {
  parentFolderId: "parentFolderId-value",
  displayName: "displayName-value"
};

let res = await client.api('/me/contactFolders/{id}')
    .update({contactFolder : contactFolder});

```