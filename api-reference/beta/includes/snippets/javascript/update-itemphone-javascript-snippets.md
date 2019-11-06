---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: c9410020445991b9c445c8e7879c43d1da2e9813
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37997341"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const itemPhone = {
  displayName: "displayName-value",
  type: "type-value",
  number: "number-value"
};

let res = await client.api('/me/profile/phones/{id}')
    .version('beta')
    .update(itemPhone);

```