---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 2c15b4be14cb52ec66602c33f5d700ced99d3a01
ms.sourcegitcommit: 239db9e961e42b505f52de9859963a9136935f2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "46821019"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var projectParticipation = new ProjectParticipation
{
    Categories = new List<String>()
    {
        "Branding"
    },
    Client = new CompanyDetail
    {
        DisplayName = "Contoso Ltd.",
        Department = "Corporate Marketing",
        WebUrl = "https://www.contoso.com"
    },
    DisplayName = "Contoso Re-branding Project",
    Detail = new PositionDetail
    {
        Company = new CompanyDetail
        {
            DisplayName = "Adventureworks Inc.",
            Department = "Consulting",
            WebUrl = "https://adventureworks.com"
        },
        Description = "Rebranding of Contoso Ltd.",
        JobTitle = "Lead PM Rebranding",
        Role = "project management",
        Summary = "A 6 month project to help Contoso rebrand after they were divested from a parent organization."
    }
};

await graphClient.Me.Profile.Projects
    .Request()
    .AddAsync(projectParticipation);

```