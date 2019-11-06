---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 6b1f9c9008051a628ec5610138d37d91498e0643
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37998956"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const directoryObject = {
    @odata.id: "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
};

let res = await client.api('/applications/{id}/owners/$ref')
    .post(directoryObject);

```