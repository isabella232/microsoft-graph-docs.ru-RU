---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 95a6ac778661e3ae64195528eba8c3c8f7a5353e
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34470362"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const device = {
  accountEnabled:false,
  alternativeSecurityIds:
  [
    {
      type:2,
      key:"base64Y3YxN2E1MWFlYw=="
    }
  ],
  deviceId:"4c299165-6e8f-4b45-a5ba-c5d250a707ff",
  displayName:"Test device",
  operatingSystem:"linux",
  operatingSystemVersion:"1"
};

let res = await client.api('/devices')
    .post({device : device});

```