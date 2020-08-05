---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 25e70f8e264335b79562adcc014b08c322171e89
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46566399"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const printTaskDefinition = {
  displayName: "Test TaskDefinitionName",
  createdBy: {
    displayName: "Requesting App Display Name"
  }
};

let res = await client.api('/print/taskDefinitions/fab143fd-ee61-4358-8558-2c7dee953982')
    .version('beta')
    .update(printTaskDefinition);

```