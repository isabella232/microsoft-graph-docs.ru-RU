---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 31a5aad70a095546c8ae12f17ec00503da8e2325
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35725741"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var history = await graphClient.RiskyUsers["41a31b00-3b3b-42d9-8f1c-6d4f14e74c69"].History
    .Request()
    .GetAsync();

```