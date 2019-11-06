---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 42e34a29538f57a9e0a9922a4aad6c7a4988d6d5
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37995950"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var contentInfo = new ContentInfo
{
    AdditionalData = new Dictionary<string, object>()
    {
        {"metadata@odata.type","#Collection(microsoft.graph.keyValuePair)"},
        {"state@odata.type","#microsoft.graph.contentState"},
        {"format@odata.type","#microsoft.graph.contentFormat"}
    },
    Format = ContentFormat.Default,
    Identifier = null,
    State = ContentState.Rest,
    Metadata = new List<KeyValuePair>()
    {
        new KeyValuePair
        {
            Name = "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Enabled",
            Value = "True"
        },
        new KeyValuePair
        {
            Name = "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Method",
            Value = "Standard"
        },
        new KeyValuePair
        {
            Name = "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SetDate",
            Value = "1/1/0001 12:00:00 AM"
        },
        new KeyValuePair
        {
            Name = "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SiteId",
            Value = "cfa4cf1d-a337-4481-aa99-19d8f3d63f7c"
        },
        new KeyValuePair
        {
            Name = "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Name",
            Value = "General"
        },
        new KeyValuePair
        {
            Name = "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ContentBits",
            Value = "0"
        },
        new KeyValuePair
        {
            Name = "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ActionId",
            Value = "00000000-0000-0000-0000-000000000000"
        }
    }
};

var downgradeJustification = new DowngradeJustification
{
    JustificationMessage = "The information has been declassified.",
    IsDowngradeJustified = true
};

await graphClient.Informationprotection.Policy.Labels
    .EvaluateRemoval(contentInfo,downgradeJustification)
    .Request()
    .PostAsync();

```