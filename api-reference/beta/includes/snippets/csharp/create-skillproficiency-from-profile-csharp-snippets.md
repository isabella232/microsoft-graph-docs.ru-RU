---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: bc5297566e7267f68368b6ada43c3c7f9dd2d1d3
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "37997773"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var skillProficiency = new SkillProficiency
{
    Categories = new List<String>()
    {
        "categories-value"
    },
    DisplayName = "displayName-value",
    Proficiency = SkillProficiencyLevel.Elementary,
    WebUrl = "webUrl-value"
};

await graphClient.Me.Profile.Skills
    .Request()
    .AddAsync(skillProficiency);

```