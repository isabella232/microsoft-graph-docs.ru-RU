---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 899cef16b608d38516189727631c35cb333cf476
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34481851"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getYammerGroupsActivityGroupCounts = await graphClient.Reports.GetYammerGroupsActivityGroupCounts('D7')
    .Request()
    .GetAsync();

```