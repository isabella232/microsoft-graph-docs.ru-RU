---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 52811b736c4a4016c221b341a721b5d75c7ba935
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48622511"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var favoritePlans = await graphClient.Me.Planner.FavoritePlans
    .Request()
    .GetAsync();

```