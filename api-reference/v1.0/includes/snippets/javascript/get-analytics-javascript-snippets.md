---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 7cdbbb60fe41438f19cb9b969be2719983421102
ms.sourcegitcommit: 0be363e309fa40f1fbb2de85b3b559105b178c0c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "44793934"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/followedSites')
    .get();

```