---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 582cec5a8053b3fe046a0f0871a63cce59ef4ab4
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48603817"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const sendMail = {
  message: {
    subject: "9/9/2018: concert",
    body: {
      contentType: "HTML",
      content: "The group represents Nevada."
    },
    toRecipients: [
      {
        emailAddress: {
          address: "AlexW@contoso.OnMicrosoft.com"
        }
      }
    ],
    internetMessageHeaders:[
      {
        name:"x-custom-header-group-name",
        value:"Nevada"
      },
      {
        name:"x-custom-header-group-id",
        value:"NV001"
      }
    ]
  }
};

let res = await client.api('/me/sendMail')
    .post(sendMail);

```