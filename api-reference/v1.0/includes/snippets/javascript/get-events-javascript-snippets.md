---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 06d9b852625acab9ebb9766d16d687b569ffe15a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35473488"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/events')
    .header('Prefer','outlook.timezone="Pacific Standard Time"')
    .select('subject,body,bodyPreview,organizer,attendees,start,end,location')
    .get();

```