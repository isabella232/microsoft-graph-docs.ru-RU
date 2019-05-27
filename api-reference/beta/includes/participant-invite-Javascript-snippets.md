---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: e0188059c57aa7cccca7ca0801ff86379fadadf5
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34443574"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const CommsOperation = {
  participants: [
    {
      endpointType: "default",
      identity: {
        user: {
          id: "550fae72-d251-43ec-868c-373732c2704f",
          tenantId: "72f988bf-86f1-41af-91ab-2d7cd011db47",
          displayName: "Heidi Steen"
        }
      },
      languageId: "languageId-value",
      region: "region-value",
      replacesCallId: "replacesCallId-value"
    }
  ],
  clientContext: "clientContext-value"
};

let res = await client.api('/app/calls/{id}/participants/invite')
    .version('beta')
    .post(CommsOperation);

```