---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 653e39f552c1009bcf1de614cc85d97041e3bb18
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527983"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var findRooms = await graphClient.Me.FindRooms('Building2Rooms@contoso.onmicrosoft.com')
    .Request()
    .GetAsync();

```