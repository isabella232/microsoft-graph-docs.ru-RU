---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 16c27500546537208385962e69011bb4cba9b421
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2020
ms.locfileid: "44052403"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const uploadSession = {
  AttachmentItem: {
    attachmentType: "file",
    name: "flower", 
    size: 3483322
  }
};

let res = await client.api('/me/messages/AAMkADI5MAAIT3drCAAA=/attachments/createUploadSession')
    .post(uploadSession);

```