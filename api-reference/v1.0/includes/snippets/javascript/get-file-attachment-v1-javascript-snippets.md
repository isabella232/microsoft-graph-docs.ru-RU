---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 1ea59b1b76d35b19f7746d5b807ba54465173f4f
ms.sourcegitcommit: f50b1feff72182d1e19bfa346304beaf29558b68
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2019
ms.locfileid: "36461836"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/events/{id}/attachments/{id}')
    .get();

```