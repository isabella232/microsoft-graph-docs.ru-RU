---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 88ecf0e2d17d4772bb82d707a4381f2438cea083
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "44681730"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var educationOutcome = new EducationRubricOutcome
{
    RubricQualityFeedback = new List<RubricQualityFeedbackModel>()
    {
        new RubricQualityFeedbackModel
        {
            QualityId = "9a145aa8-f3d9-43a1-8f77-5387ff0693f2",
            Feedback = new EducationItemBody
            {
                Content = "This is feedback specific to the first quality of the rubric.",
                ContentType = BodyType.Text
            }
        },
        new RubricQualityFeedbackModel
        {
            QualityId = "d2331fb2-2761-402e-8de6-93e0afaa076e",
            Feedback = new EducationItemBody
            {
                Content = "This is feedback specific to the second quality of the rubric.",
                ContentType = BodyType.Text
            }
        }
    },
    RubricQualitySelectedLevels = new List<RubricQualitySelectedColumnModel>()
    {
        new RubricQualitySelectedColumnModel
        {
            QualityId = "9a145aa8-f3d9-43a1-8f77-5387ff0693f2",
            ColumnId = "4fb17a1d-5681-46c2-a295-4e305c3eae23"
        },
        new RubricQualitySelectedColumnModel
        {
            QualityId = "d2331fb2-2761-402e-8de6-93e0afaa076e",
            ColumnId = "aac076bf-51ba-48c5-a2e0-ee235b0b9740"
        }
    }
};

await graphClient.Education.Me.Assignments["{id}"].Submissions["{id}"].Outcomes["{id}"]
    .Request()
    .UpdateAsync(educationOutcome);

```