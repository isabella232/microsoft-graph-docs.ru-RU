---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 99cc4142fd1fc9a2f720615728a6f780de6fec97
ms.sourcegitcommit: 0e1101d499f35b08aa2309e273871438b1774979
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2019
ms.locfileid: "35335090"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/businessFlowTemplates')
    .version('beta')
    .get();

```