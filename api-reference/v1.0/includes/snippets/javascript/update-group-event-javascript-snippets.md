---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 1c9bc81f713a268d73888a3b86927986bb811650
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35515950"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const event = {
  location:{
      displayName:"Conf Room 2"
  }
};

let res = await client.api('/groups/01d4ee64-15ce-491e-bad1-b91aa3223df4/calendar/events/AAMkADZlAAAAABERAAA=')
    .update({event : event});

```