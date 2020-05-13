---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 89e842b5aab5014af97fcf65422d22f047c0d7a1
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2020
ms.locfileid: "44216793"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var printIdentity = new PrintIdentity
{
    AdditionalData = new Dictionary<string, object>()
    {
        {"@odata.id","https://graph.microsoft.com/beta/groups/{id}"}
    }
};

await graphClient.Print.Shares["{id}"].AllowedGroups.References
    .Request()
    .AddAsync(printIdentity);

```