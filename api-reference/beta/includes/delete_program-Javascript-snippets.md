---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 1cda4bb270f4b6ff75a859566b8f118ed430dc1e
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34437603"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/programs/7e59d237-2fb0-4e5d-b7bb-d4f9f9129213')
    .version('beta')
    .delete();

```