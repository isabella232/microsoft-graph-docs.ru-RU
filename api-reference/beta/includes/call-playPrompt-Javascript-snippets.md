---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 99f15b1f3a3f260e21f4502fc5df286c413dc286
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34456258"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const CommsOperation = {
  clientContext: "d45324c1-fcb5-430a-902c-f20af696537c",
  prompts: [
    {
      @odata.type: "#microsoft.graph.mediaPrompt",
      mediaInfo: {
        uri: "https://cdn.contoso.com/beep.wav",
        resourceId: "1D6DE2D4-CD51-4309-8DAA-70768651088E"
      },
      loop: 5
    }
  ]
};

let res = await client.api('/app/calls/{id}/playPrompt')
    .version('beta')
    .post(CommsOperation);

```