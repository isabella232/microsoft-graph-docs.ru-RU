---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 32c9c758f2e9966058251aae4b7ec2a95c2bda69
ms.sourcegitcommit: 94c8985a3956622ea90f7e641f894d57b0982eb9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2020
ms.locfileid: "44217637"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String message = "Sorry, you can't offer this shift.";

graphClient.teams("{teamId}").schedule().offerShiftRequests("{offerShiftRequestId}")
    .decline(message)
    .buildRequest()
    .post();

```