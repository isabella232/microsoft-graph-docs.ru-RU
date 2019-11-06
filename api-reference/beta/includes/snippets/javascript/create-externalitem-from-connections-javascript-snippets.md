---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 34ed1f0208deca5f0325f10297fea78b4b13629e
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37994574"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const externalItem = {
  @odata.type: "microsoft.graph.externalItem",
  acl: [
    {
      type: "user",
      value: "49103559-feac-4575-8b94-254814dfca72",
      accessType: "deny",
      identitySource: "Azure Active Directory"
    }
  ],
  properties: {
    title: "Error in the payment gateway",
    priority: 1,
    assignee: "john@contoso.com"
  },
  content: "Textual content of the file"
};

let res = await client.api('/connections/contosohr/items/TSP228082938')
    .version('beta')
    .put(externalItem);

```