---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d04a191acfed67716ccb700b1d369fbfc45b87d0
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "44684955"
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
    .Select("subject,bodyPreview,seriesMasterId,type,recurrence,start,end")
    .GetAsync();

```