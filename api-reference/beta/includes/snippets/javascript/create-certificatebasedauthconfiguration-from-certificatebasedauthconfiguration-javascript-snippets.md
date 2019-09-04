---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d70c8900c97d93c27969fec05a951461786fbe74
ms.sourcegitcommit: d1742ec820776f1e95cba76d98c6cfd17d3eadbb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/04/2019
ms.locfileid: "36720103"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const certificateBasedAuthConfiguration = {
  certificateAuthorities: [
    {
      isRootAuthority: true,
      certificate: "Binary"
    }
  ]
};

let res = await client.api('/organization/{id}/certificateBasedAuthConfiguration')
    .version('beta')
    .post(certificateBasedAuthConfiguration);

```