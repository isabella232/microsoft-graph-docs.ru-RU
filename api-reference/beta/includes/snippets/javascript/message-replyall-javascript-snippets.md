---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 35c23382325e1ff96a1735d7f30e80ce58bb5c1e
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48619064"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const replyAll = {
    message:{
      attachments: [ 
        { 
          @odata.type: "#microsoft.graph.fileAttachment", 
          name: "guidelines.txt", 
          contentBytes: "bWFjIGFuZCBjaGVlc2UgdG9kYXk=" 
        } 
      ]
    },
    comment: "Please take a look at the attached guidelines before you decide on the name." 
};

let res = await client.api('/me/messages/AAMkADA1MTAAAH5JaKAAA=/replyAll')
    .version('beta')
    .post(replyAll);

```