---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ed2bb061ef847d5cf854faa44ca94a936ae471f1
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35710321"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var application = await graphClient.Applications["{id}"]
    .Request()
    .GetAsync();

```