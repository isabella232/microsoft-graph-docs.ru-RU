---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: fb345d8ac1c25ff29197cb7646da7af78261c627
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34479709"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var directReports = await graphClient.Me.DirectReports
    .Request()
    .GetAsync();

```