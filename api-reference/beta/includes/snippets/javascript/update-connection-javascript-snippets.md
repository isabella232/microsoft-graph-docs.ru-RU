---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 1652efab37b1933f6748d60140e6c0ef7f912aa8
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37994531"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const externalConnection = {
  name: "Contoso HR Service Tickets",
  description: "Connection to index HR service tickets"
};

let res = await client.api('/connections/contosohr')
    .version('beta')
    .update(externalConnection);

```