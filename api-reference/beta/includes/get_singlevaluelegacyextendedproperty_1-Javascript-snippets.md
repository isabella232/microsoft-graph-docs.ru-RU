---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 646445391bc06cf2dca8a1b041c4a226bb2ac2a3
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34445968"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/messages/AAMkAGE1M2_bs88AACHsLqWAAA=/')
    .version('beta')
    .filter('id eq 'String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color')')
    .expand('singleValueExtendedProperties($filter=id%20eq%20'String%20%7B66f5a359-4659-4830-9070-00047ec6ac6e%7D%20Name%20Color')')
    .get();

```