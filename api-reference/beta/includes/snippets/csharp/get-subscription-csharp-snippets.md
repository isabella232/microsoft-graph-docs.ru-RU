---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ff80ff9b4fb36607e2bf97d3d1c9f8842cbb79d7
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35717494"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var subscription = await graphClient.Subscriptions["{id}"]
    .Request()
    .GetAsync();

```