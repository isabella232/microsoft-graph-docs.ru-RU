---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ace51b29cd55ff6ee7d157012ee4df78de43264a
ms.sourcegitcommit: 8e18d7fe3c869b2fd48872365116175d3bdce1b7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2020
ms.locfileid: "46643869"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/applicationTemplates')
    .version('beta')
    .get();

```