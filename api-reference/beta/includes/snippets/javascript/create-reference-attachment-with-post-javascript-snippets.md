---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a22397f25bb0fecc8e4e2132f6956792e96d5f00
ms.sourcegitcommit: d8a425766aa6a56027b8576bbec6a9d1ae3e079c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "36633554"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const reply = {
  post: {
    body: {
      contentType: "text",
      content: "I attached a reference to a file on OneDrive."
    },
    attachments: [{
      @odata.type: "#microsoft.graph.referenceAttachment", 
      name: "Personal pictures", 
      sourceUrl: "https://contoso.com/personal/mario_contoso_net/Documents/Pics", 
      providerType: "oneDriveConsumer", 
      permission: "Edit", 
      isFolder: "True"
    } ]
  }
};

let res = await client.api('/groups/1848753d-185d-4c08-a4e4-6ee40521d115/threads/AAQkADJUdfolA==/reply')
    .version('beta')
    .post(reply);

```