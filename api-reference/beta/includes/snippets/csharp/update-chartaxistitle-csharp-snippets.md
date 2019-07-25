---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 51f4ee31463669770147dc0f46af2153d055d515
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35708317"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookChartAxisTitle = new WorkbookChartAxisTitle
{
    Text = "text-value",
    Visible = true
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Axes.ValueAxis.Title
    .Request()
    .UpdateAsync(workbookChartAxisTitle);

```