---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: b0a005b3623b82538daa5872e9e0b443dd8784a1
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34479912"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/directoryRoles/{id}')
    .get();

```