---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 8fa0781d816770a6270913fde35c85c6ff1c74cc
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35529549"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/subscriptions')
    .version('beta')
    .get();

```