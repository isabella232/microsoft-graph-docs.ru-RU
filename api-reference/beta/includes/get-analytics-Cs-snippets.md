---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 52a38fd810ddb7b620da211155c84160f6689fcc
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34436546"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var itemAnalytics = await graphClient.Drives["{drive-id}"].Items["{item-id}"].Analytics
    .Request()
    .GetAsync();

```