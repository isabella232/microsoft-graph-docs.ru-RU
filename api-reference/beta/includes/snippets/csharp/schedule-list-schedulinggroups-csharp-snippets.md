---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 4a5571c2af1d29ce8dff963a70bd3259c8f06f18
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48612832"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var schedulingGroups = await graphClient.Teams["{teamId}"].Schedule.SchedulingGroups
    .Request()
    .GetAsync();

```