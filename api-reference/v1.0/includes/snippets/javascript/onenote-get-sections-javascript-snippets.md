---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 398ab8439e89bb308cd275f7f09b5833a4b84a37
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35887996"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/onenote/sections')
    .get();

```