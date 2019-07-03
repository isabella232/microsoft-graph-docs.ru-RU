---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 07cf54822bd266657d8526f7c20e0c27c33c176c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35505226"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var educationAssignment = new EducationAssignment
{
    DisplayName = "Week 1 reading assignment",
    Instructions = new EducationItemBody
    {
        ContentType = BodyType.Text,
        Content = "Read chapters 1 through 3"
    },
    DueDateTime = "2014-02-01T00:00:00Z"
};

await graphClient.Education.Classes["11021"].Assignments["19002"]
    .Request()
    .UpdateAsync(educationAssignment);

```