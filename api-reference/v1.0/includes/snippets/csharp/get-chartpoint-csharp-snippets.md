---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 170e4175d24833cf2e3e89d55df871297dcdc05b
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48618250"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookChartPoint = await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Series["{series-id}"].Points["{point-id}"]
    .Request()
    .GetAsync();

```