---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ce96b62f2bb24068ab318fb39bb9cce0454a284c
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35880612"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookRangeFormat = await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"]
    .Range().Format
    .Request()
    .GetAsync();

```