---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 2480e82825922c41a4fa4af8ef76493fe976093e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35529530"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookWorksheet = await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"]
    .Request()
    .GetAsync();

```