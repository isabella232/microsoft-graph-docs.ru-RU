---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: fe2e94f1e9bcfc56060bdbbe9ce4befe97c8fdff
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35505347"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const directoryObject = {
  directoryObject: {
  }
};

let res = await client.api('/applications/{id}/owners')
    .version('beta')
    .post({directoryObject : directoryObject});

```