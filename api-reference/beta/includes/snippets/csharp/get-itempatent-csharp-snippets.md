---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ea72ab418a79234bf4a98a50301de50d55c1f9af
ms.sourcegitcommit: 239db9e961e42b505f52de9859963a9136935f2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "46819930"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var itemPatent = await graphClient.Me.Profile.Patents["{id}"]
    .Request()
    .GetAsync();

```