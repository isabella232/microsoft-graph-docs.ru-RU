---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: aedee0f168d83cacc6a98178351d9b2428ed7b9c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35488608"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const message = {
  subject: "Annual review",
  body: {
    contentType: "HTML",
    content: "You should be proud!"
  },
  toRecipients: [
    {
      emailAddress: {
        address: "rufus@contoso.com"
      }
    }
  ],
  extensions: [
    {
      @odata.type: "microsoft.graph.openTypeExtension",
      extensionName: "Com.Contoso.Referral",
      companyName: "Wingtip Toys",
      expirationDate: "2015-12-30T11:00:00.000Z",
      dealValue: 10000
    }
  ]
};

let res = await client.api('/me/messages')
    .version('beta')
    .post({message : message});

```