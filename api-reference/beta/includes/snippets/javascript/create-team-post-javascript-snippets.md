---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: bc5528f4e615a8d99b3e441620b3a874cf240a41
ms.sourcegitcommit: 5a1373f2ccd9ee813fc60d42e7ac6b115b5f9f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "44335536"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const team = {
  template@odata.bind: "https://graph.microsoft.com/beta/teamsTemplates('standard')",
  displayName: "My Sample Team",
  description: "My Sample Team’s Description"
};

let res = await client.api('/teams')
    .version('beta')
    .post(team);

```