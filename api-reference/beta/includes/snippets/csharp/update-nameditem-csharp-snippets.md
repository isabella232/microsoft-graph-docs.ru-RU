---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 345b3f03bd61d072796099643d122d9541bcbd55
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "44684330"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookNamedItem = new WorkbookNamedItem
{
    Type = "type-value",
    Scope = "scope-value",
    Comment = "comment-value",
    Value = JToken.Parse("{}"),
    Visible = true
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"]
    .Request()
    .UpdateAsync(workbookNamedItem);

```