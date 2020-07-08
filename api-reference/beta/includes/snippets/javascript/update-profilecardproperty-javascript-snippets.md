---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 08c4841250f75090e7f00e982c9d8a1e59928851
ms.sourcegitcommit: 2050639c9e9a6b2dab9ce53d6a9fc87e98789b50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/08/2020
ms.locfileid: "45080669"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const customAttribute1 = {
  annotations: [
    {
      localizations: [
        {
          languageTag: "no-NB",
          displayName: "Kostnads Senter"
        }
      ]
    }
  ]
};

let res = await client.api('/organization/settings/profileCardProperties/CustomAttribute1')
    .version('beta')
    .update(customAttribute1);

```