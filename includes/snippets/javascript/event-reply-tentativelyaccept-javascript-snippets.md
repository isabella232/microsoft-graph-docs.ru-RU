---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ca6c9d0a57a5a77c53a6208690948542a44d3e87
ms.sourcegitcommit: 7b286637aa332cfd534a41526950b4f6272e0fd7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "41774721"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const tentativelyAccept = {
  comment: "I will probably be able to make it.",
  sendResponse: true
};

let res = await client.api('/me/events/AAMkADADVj3fyAABZ5ieyAAA=/tentativelyAccept')
    .post(tentativelyAccept);

```