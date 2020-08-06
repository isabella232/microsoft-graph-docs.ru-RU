---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 7d812b80e052592663821f7f07b1a2de7e755a50
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46567367"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const namedLocation = {
    @odata.type: "#microsoft.graph.ipNamedLocation",
    displayName: "Untrusted named location with only IPv4 address",
    isTrusted: false,
    ipRanges: [
        {
            @odata.type: "#microsoft.graph.iPv4CidrRange",
            cidrAddress: "6.5.4.3/18"
        }

    ]
};

let res = await client.api('/identity/conditionalAccess/namedLocations/0854951d-5fc0-4eb1-b392-9b2c9d7949c2')
    .update(namedLocation);

```