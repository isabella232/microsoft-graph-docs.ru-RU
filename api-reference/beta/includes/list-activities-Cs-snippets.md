---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 360ebe3b06dcd09e484bff21fe3637cf7772d6ad
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34444484"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var activities = await graphClient.Me.Drive.Activities
    .Request()
    .GetAsync();

```