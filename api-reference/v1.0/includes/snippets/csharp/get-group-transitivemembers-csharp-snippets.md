---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f06acd154b19fbc5676645059d41fe9e6e612be3
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48609349"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var transitiveMembers = await graphClient.Groups["{id}"].TransitiveMembers
    .Request()
    .GetAsync();

```