---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 5b8cb8f5fa1c29c3946255ebb311adaceec70c12
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "36365578"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var persistChanges = true;

await graphClient.Me.Drive.Items["{id}"].Workbook
    .CreateSession(persistChanges)
    .Request()
    .PostAsync();

```