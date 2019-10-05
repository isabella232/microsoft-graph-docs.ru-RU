---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: b7d47aa4f14c39efe5cf4034b19449b161aaacb2
ms.sourcegitcommit: 46ee19b244349e2a1537f0c44c576d7c01cf03a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/05/2019
ms.locfileid: "37402314"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var targets = new List<InvitationParticipantInfo>()
{
    new InvitationParticipantInfo
    {
        EndpointType = EndpointType.Default,
        Identity = new IdentitySet
        {
            User = new Identity
            {
                Id = "550fae72-d251-43ec-868c-373732c2704f",
                TenantId = "72f988bf-86f1-41af-91ab-2d7cd011db47",
                DisplayName = "Heidi Steen"
            }
        },
        LanguageId = "en-US",
        Region = "westus"
    }
};

var targetDisposition = CallDisposition.Default;

var timeout = 99;

var maskCallee = false;

var maskCaller = false;

await graphClient.App.Calls["{id}"]
    .Redirect(targets,targetDisposition,timeout,maskCallee,maskCaller,null)
    .Request()
    .PostAsync();

```