---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ed0241b04cfa338678a26ad976b9ff579c4a003e
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48952908"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const informationProtectionAction = {
  contentInfo: {
    @odata.type: "#microsoft.graph.contentInfo",
    format@odata.type: "#microsoft.graph.contentFormat",
    format: "default",
    identifier: null,
    state@odata.type: "#microsoft.graph.contentState",
    state: "rest",
    metadata@odata.type: "#Collection(microsoft.graph.keyValuePair)",
    metadata: [
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Enabled",
        value: "True"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Method",
        value: "Standard"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SetDate",
        value: "1/1/0001 12:00:00 AM"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SiteId",
        value: "cfa4cf1d-a337-4481-aa99-19d8f3d63f7c"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Name",
        value: "General"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ContentBits",
        value: "0"
      },
      {
        @odata.type: "#microsoft.graph.keyValuePair",
        name: "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ActionId",
        value: "00000000-0000-0000-0000-000000000000"
      }
    ]
  },
  downgradeJustification: {
        justificationMessage: "The information has been declassified.",
        isDowngradeJustified: true
    }
};

let res = await client.api('/informationProtection/policy/labels/evaluateRemoval')
    .version('beta')
    .post(informationProtectionAction);

```