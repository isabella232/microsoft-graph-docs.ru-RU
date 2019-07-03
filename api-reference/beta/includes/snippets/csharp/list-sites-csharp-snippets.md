---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 43e9656defd20f99a9b92b4a6c47e27fba764600
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35528392"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var queryOptions = new List<QueryOption>()
{
    new QueryOption("select", "siteCollection,webUrl"),
    new QueryOption("filter", "siteCollection/root ne null")
};

var sites = await graphClient.Sites
    .Request( queryOptions )
    .Filter("siteCollection/root ne null")
    .GetAsync();

```