---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 4b1e068ad2c1150e8326a30d30f298735f800da9
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48974329"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

TodoTask todoTask = new TodoTask();
DateTimeTimeZone dueDateTime = new DateTimeTimeZone();
dueDateTime.dateTime = "2020-07-25T16:00:00";
dueDateTime.timeZone = "Eastern Standard Time";
todoTask.dueDateTime = dueDateTime;

graphClient.me().todo().lists("AAMkADA1MTHgwAAA=").tasks("721a35e2-35e2-721a-e235-1a72e2351a72")
    .buildRequest()
    .patch(todoTask);

```