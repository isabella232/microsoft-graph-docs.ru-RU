---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 15fc8f8a746d4fbeafc853f76d46d74a3e45a06d
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34453616"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const conversationThread = {
  topic: "topic-value",
  posts: [{
      body: {
        contentType: "html",
        content: "this is body content"
      }
  }]
};

let res = await client.api('/groups/{id}/conversations/{id}/threads')
    .version('beta')
    .post({conversationThread : conversationThread});

```