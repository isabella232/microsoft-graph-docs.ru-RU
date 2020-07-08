---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 8f0903d8a9930b97f67777aaa8c10ce0ccfc8e08
ms.sourcegitcommit: 2050639c9e9a6b2dab9ce53d6a9fc87e98789b50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/08/2020
ms.locfileid: "45081079"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const printer = {
  displayName: "Test Printer",
  manufacturer: "Test Printer Manufacturer",
  model: "Test Printer Model",
  physicalDeviceId: null,
  hasPhysicalDevice: false,
  certificateSigningRequest: { 
    content: "{content}",
    transportKey: "{sampleTransportKey}"
  },
  connectorId: null
};

let res = await client.api('/print/printers/create')
    .version('beta')
    .post(printer);

```