---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 2474b3e27a65d1cd36139d4e4301b23b2cd6751c
ms.sourcegitcommit: 94c8985a3956622ea90f7e641f894d57b0982eb9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2020
ms.locfileid: "44219303"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = "message-value";

await graphClient.Teams["{teamId}"].Schedule.SwapShiftsChangeRequests["{swapShiftChangeRequestId}"]
    .Decline(message)
    .Request()
    .PostAsync();

```