---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 75e86664fd0770db8f0cbdf6413e44924624b836
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40870468"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const workforceIntegrations = {
  displayName: "displayName-value",
  apiVersion: 99,
  encryption: {
    protocol: "protocol-value",
    secret: "secret-value"
  },
  isActive: true,
  url: "url-value",
  supports: "supports-value"
};

let res = await client.api('/teamwork/workforceIntegrations')
    .version('beta')
    .update(workforceIntegrations);

```