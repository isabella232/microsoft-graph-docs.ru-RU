---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 1772f529ad59522ae52141e034559145d92d81fb
ms.sourcegitcommit: 33ffed5b785abf36b1a7786856c9266958830d25
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2020
ms.locfileid: "42947738"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const printer = {
  name: "PrinterName",
  location: {
    latitude: 1.1,
    longitude: 2.2,
    altitudeInMeters: 3
  }
};

let res = await client.api('/print/printers/{id}')
    .version('beta')
    .update(printer);

```