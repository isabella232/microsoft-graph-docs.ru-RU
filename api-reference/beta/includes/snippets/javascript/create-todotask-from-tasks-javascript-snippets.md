---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 38ac27b67ceeb1468d39e9364f36363113019084
ms.sourcegitcommit: c20276369a8834a259f24038e7ee5c33de02660b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/07/2020
ms.locfileid: "48375671"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const todoTask = {
   title:"A new task",
   linkedResources:[
      {
         webUrl:"http://microsoft.com",
         applicationName:"Microsoft",
         displayName:"Microsoft"
      }
   ]
};

let res = await client.api('/me/todo/lists/AQMkADAwATM0MDAAMS0yMDkyLWVjMzYtM/tasks')
    .version('beta')
    .post(todoTask);

```