---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d229f6306cee32267c60590661d8427ebd1dded1
ms.sourcegitcommit: c0df90d66cb2072848d4bb0bf730c47a601b99ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34536710"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var queryOptions = new List<QueryOption>()
{
    new QueryOption("startDateTime", "2019-04-08T09:00:00.0000000"),
    new QueryOption("endDateTime", "2019-04-30T09:00:00.0000000")
};

var instances = await graphClient.Me.Events["AAMkAGUzYRgWAAA="].Instances
    .Request( queryOptions )
    .Select( e => new {
             e.Subject,
             e.BodyPreview,
             e.SeriesMasterId,
             e.Type,
             e.Recurrence,
             e.Start,
             e.End 
             })
    .GetAsync();

```