---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a9e655ef561c1ec5e7b99881dc4625e4a165bde3
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40870616"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/teamwork/workforceIntegrations')
    .version('beta')
    .get();

```