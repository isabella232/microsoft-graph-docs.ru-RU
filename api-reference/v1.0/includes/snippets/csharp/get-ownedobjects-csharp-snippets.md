---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 2959b6731cceca6353c3a0c160ed0881e20d36e2
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35515277"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var ownedObjects = await graphClient.Me.OwnedObjects
    .Request()
    .GetAsync();

```