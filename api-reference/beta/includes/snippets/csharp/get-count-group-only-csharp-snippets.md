---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a97e3b924e5ed0fbd191bb454358af18c3f6d36a
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "44685114"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var int32 = await graphClient.ServicePrincipals["{id}"].MemberOf.$count
    .Request()
    .Header("ConsistencyLevel","eventual")
    .GetAsync();

```