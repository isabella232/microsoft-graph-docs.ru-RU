---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 506840739597e2e1eba8f6a4c10a4292c8f688d6
ms.sourcegitcommit: c20276369a8834a259f24038e7ee5c33de02660b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/07/2020
ms.locfileid: "48373499"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const channel = {
  @odata.type: "#Microsoft.Graph.channel",
  membershipType: "private",
  displayName: "My First Private Channel",
  description: "This is my first private channels",
  members:
     [
        {
           @odata.type:"#microsoft.graph.aadUserConversationMember",
           user@odata.bind:"https://graph.microsoft.com/v1.0/users('{user_id}')",
           roles:["owner"]
        }
     ]
};

let res = await client.api('/teams/{group_id}/channels')
    .post(channel);

```