---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 66b29d9d5af28780e0e8278c528722c3dcb22f57
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48975925"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IUserReminderViewCollectionPage reminderView = graphClient.me()
    .reminderView("2017-06-05T10:00:00.0000000","2017-06-11T11:00:00.0000000")
    .buildRequest()
    .get();

```