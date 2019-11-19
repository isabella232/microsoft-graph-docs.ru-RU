---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 12e67bfa9f6242cc85168f59822b57778ccdd99f
ms.sourcegitcommit: ef8eac3cf973a1971f8f1d41d75a085fad3690f0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2019
ms.locfileid: "37996400"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var requests = new List<SearchRequest>()
{
    new SearchRequest
    {
        EntityTypes = new List<EntityType>()
        {
            EntityType.Event
        },
        ContentSources = new List<String>()
        {
            "/external/connections/connectionfriendlyname"
        },
        Query = new SearchQuery
        {
            Query_string = new SearchQueryString
            {
                Query = "contoso product"
            }
        },
        From = 0,
        Size = 25,
        Stored_fields = new List<String>()
        {
            "title",
            "description"
        }
    }
};

await graphClient.Search
    .Query(requests)
    .Request()
    .PostAsync();

```