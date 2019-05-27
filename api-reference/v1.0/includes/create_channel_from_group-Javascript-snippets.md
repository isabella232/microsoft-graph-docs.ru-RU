---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 9baee5663c32ba934ae21a4403fe7498245bb364
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34480087"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const channel = {
  displayName: "Architecture Discussion",
  description: "This channel is where we debate all future architecture plans"
};

let res = await client.api('/teams/{id}/channels')
    .post({channel : channel});

```