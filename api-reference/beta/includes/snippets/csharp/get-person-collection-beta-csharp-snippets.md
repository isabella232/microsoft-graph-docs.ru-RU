---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a7ec8819005c21715473378fe105484d3c0f26e6
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35716508"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var people = await graphClient.Me.People
    .Request()
    .GetAsync();

```