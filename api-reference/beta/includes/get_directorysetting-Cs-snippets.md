---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d23dc968d33e2279a2ec6f270756ca6a96738296
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34471931"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var directorySetting = await graphClient.Settings["{id}"]
    .Request()
    .GetAsync();

```