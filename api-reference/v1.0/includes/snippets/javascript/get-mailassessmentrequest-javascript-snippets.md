---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a169167f8ef964d31c110dcb3be62d14b1a70169
ms.sourcegitcommit: 9edfcf99706c8490cd5832a1c706a88a89e24db1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/07/2020
ms.locfileid: "42858874"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/informationProtection/threatAssessmentRequests/49c5ef5b-1f65-444a-e6b9-08d772ea2059')
    .get();

```