---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d83ae0fd5557cc9b0f39872f62feb6a0dba59b59
ms.sourcegitcommit: 94c8985a3956622ea90f7e641f894d57b0982eb9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2020
ms.locfileid: "44218189"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String message = "Approved!";

graphClient.teams("{teamId}").schedule().offerShiftRequests("{offerShiftRequestId}")
    .approve(message)
    .buildRequest()
    .post();

```