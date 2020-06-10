---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 0de78ff6e0b358ef291d104bd0a0250761294341
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "44684397"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var plannerAssignedToTaskBoardTaskFormat = new PlannerAssignedToTaskBoardTaskFormat
{
    OrderHintsByAssignee = new PlannerOrderHintsByAssignee
    {
        AdditionalData = new Dictionary<string, object>()
        {
            {"aaa27244-1db4-476a-a5cb-004607466324", "8566473P 957764Jk!"}
        }
    }
};

await graphClient.Planner.Tasks["01gzSlKkIUSUl6DF_EilrmQAKDhh"].AssignedToTaskBoardFormat
    .Request()
    .Header("If-Match","W/\"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc=\"")
    .UpdateAsync(plannerAssignedToTaskBoardTaskFormat);

```