---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 668dd8b1a440b3a2d9e59df6fc41ac0b85ff80ae
ms.sourcegitcommit: 94c8985a3956622ea90f7e641f894d57b0982eb9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2020
ms.locfileid: "35718259"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var schedule = await graphClient.Teams["{teamId}"].Schedule
    .Request()
    .GetAsync();

```