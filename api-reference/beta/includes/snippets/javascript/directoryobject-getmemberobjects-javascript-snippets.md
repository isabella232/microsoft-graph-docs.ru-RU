---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 33f10e9e477e0b44f5612c3b22c72e14cba1c0a4
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35529925"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const String = {
  securityEnabledOnly: true
};

let res = await client.api('/me/getMemberObjects')
    .version('beta')
    .post(String);

```