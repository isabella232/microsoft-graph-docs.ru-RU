---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 2b2a93e8f7f01c68c659c503764cabf938ba22df
ms.sourcegitcommit: 1585d55d3e7030b5fd1f7cfd5de8f9fb8202cd56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2019
ms.locfileid: "37429182"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const string = {
  securityEnabledOnly: true
};

let res = await client.api('/contacts/{id}/getMemberGroups')
    .version('beta')
    .post(string);

```