---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: bf83557267af715e32ff4fc6cea732611f5ba39e
ms.sourcegitcommit: 239db9e961e42b505f52de9859963a9136935f2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "46819853"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const personWebsite = {
  description: "Lyn Damer play in the Women's 1st Division (Toppserien) in Norway"
};

let res = await client.api('/me/profile/websites/{id}')
    .version('beta')
    .update(personWebsite);

```