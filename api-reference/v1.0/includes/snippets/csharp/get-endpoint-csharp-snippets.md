---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: e95994522b0548f957101f3ff5be2408cb42847f
ms.sourcegitcommit: 5a1373f2ccd9ee813fc60d42e7ac6b115b5f9f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "44336190"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var endpoint = await graphClient.Groups["{id}"].Endpoints["{id}"]
    .Request()
    .GetAsync();

```