---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 6c801d93e949b5aa883ab18719c1b4ca9aed6f8f
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35488928"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var organization = await graphClient.Organization
    .Request()
    .GetAsync();

```