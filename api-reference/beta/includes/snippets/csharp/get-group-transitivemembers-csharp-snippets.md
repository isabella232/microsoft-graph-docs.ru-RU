---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f06acd154b19fbc5676645059d41fe9e6e612be3
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35505205"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var transitiveMembers = await graphClient.Groups["{id}"].TransitiveMembers
    .Request()
    .GetAsync();

```