---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 7bc476e2d5515e4ca7ac0b88ec8f80c558278ba3
ms.sourcegitcommit: bd40e302ce04b686e86989246ab7c4cc9ad3f320
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/03/2020
ms.locfileid: "43127198"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Identity.ConditionalAccess.NamedLocations["1c4427fd-0885-4a3d-8b23-09a899ffa959"]
    .Request()
    .DeleteAsync();

```