---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 256e053ed38bfb598498fe27536b59485d31008c
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34449463"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var identityRiskEvent = await graphClient.IdentityRiskEvents["ec50e9fb-9da1-215b-e18c-b7e2a716b2a6-c2b6c2b9-dddc-acd0-2b39-d519d803dbc3-db69711e-9324-ec99-f010-6e63fb972e98"]
    .Request()
    .GetAsync();

```