---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: aa4c4b7665e612562d6e6765310d1050dc2f0ccf
ms.sourcegitcommit: 0329bbcd5f1b09a2a6c5f935a30c4560b6eed492
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "36634056"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var attachment = new Attachment
{
    AdditionalData = new Dictionary<string, object>()
    {
        {"@odata.type","#microsoft.graph.fileAttachment"}
    },
    Name = "name-value",
    ContentBytes = "contentBytes-value"
};

await graphClient.Groups["{id}"].Threads["{id}"].Posts["{id}"].Attachments
    .Request()
    .AddAsync(attachment);

```