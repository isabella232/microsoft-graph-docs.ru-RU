---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ff2849f23da9b870be81a80f9db9c1428283caed
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48616927"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var photos = await graphClient.Groups["{id}"].Photos
    .Request()
    .GetAsync();

```