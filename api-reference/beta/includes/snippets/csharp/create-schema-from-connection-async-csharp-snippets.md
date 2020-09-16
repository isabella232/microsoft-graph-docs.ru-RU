---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 5a9fc2b437355e20db55e90e1b445054f5ff5bf9
ms.sourcegitcommit: 7e1993d64cc6d3145ae0ca984fefe74772b6052b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2020
ms.locfileid: "47938377"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var schema = new Schema
{
    BaseType = "microsoft.graph.externalItem",
    Properties = new List<Property>()
    {
        new Property
        {
            Name = "ticketTitle",
            Type = PropertyType.String,
            IsSearchable = true,
            IsRetrievable = true,
            Labels = new List<Label>()
            {
                Label.Title
            }
        },
        new Property
        {
            Name = "priority",
            Type = PropertyType.String,
            IsQueryable = true,
            IsRetrievable = true,
            IsSearchable = false
        },
        new Property
        {
            Name = "assignee",
            Type = PropertyType.String,
            IsRetrievable = true
        }
    }
};

await graphClient.External.Connections["contosohr"].Schema
    .Request()
    .Header("Prefer","respond-async")
    .AddAsync(schema);

```