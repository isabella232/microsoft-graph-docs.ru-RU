---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: cb8d13be34562c90e8b3644b66e5dfce2de4b969
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34437365"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/trustFramework/policies/B2C_1A_SocialAndLocalAccounts_Base')
    .version('beta')
    .delete();

```