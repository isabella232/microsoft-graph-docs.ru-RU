---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 4d62230fa4ed48fb11d981f704cfa94e9f707a3c
ms.sourcegitcommit: ef47b165f7a140cfc0309a275cb8722dd265660d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/25/2020
ms.locfileid: "46873222"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var aAMkADIyAAAAABrJAAA= = await graphClient.Me.Todo.Lists.AAMkADIyAAAAABrJAAA=
    .Request()
    .GetAsync();

```