---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 35b88d21c7f7f6fc59e72e629de0c670ab46c130
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496633"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const conversationThread = {
  @odata.type:"#Microsoft.OutlookServices.ConversationThread",
  isLocked: true
};

let res = await client.api('/groups/{id}/threads/{id}')
    .update({conversationThread : conversationThread});

```