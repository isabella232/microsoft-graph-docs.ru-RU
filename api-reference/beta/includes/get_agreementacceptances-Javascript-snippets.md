---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: abaae7631defb1fb4d1526be6f09ada2cdb61cb2
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34474172"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/agreementAcceptances')
    .version('beta')
    .get();

```