---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 6c3a28b8ba4b6127fbc5dcc70daff294da3ca6ea
ms.sourcegitcommit: 726f20403323be7d267b67c2764ed7c244e02ee1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "47329766"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var b2cIdentityUserFlow = await graphClient.Identity.B2cUserFlows["{id}"]
    .Request()
    .GetAsync();

```