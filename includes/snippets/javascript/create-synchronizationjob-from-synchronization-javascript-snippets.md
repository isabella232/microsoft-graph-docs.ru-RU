---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 30580a28801c4cbc3f2edf0c0d722e6304789803
ms.sourcegitcommit: 8e18d7fe3c869b2fd48872365116175d3bdce1b7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2020
ms.locfileid: "46643868"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const synchronizationJob = {
    templateId: "aws"
};

let res = await client.api('/servicePrincipals/{id}/synchronization/jobs')
    .version('beta')
    .post(synchronizationJob);

```