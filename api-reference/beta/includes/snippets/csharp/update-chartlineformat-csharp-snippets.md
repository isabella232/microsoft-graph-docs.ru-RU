---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 78a2ad327cba2d6aec1a335e27d52605dade3b74
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35708011"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookChartLineFormat = new WorkbookChartLineFormat
{
    Color = "color-value"
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Axes.SeriesAxis.Format.Line
    .Request()
    .UpdateAsync(workbookChartLineFormat);

```