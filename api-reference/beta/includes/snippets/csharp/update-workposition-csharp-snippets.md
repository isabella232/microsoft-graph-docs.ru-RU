---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: b32b90c1f578128459ea3cd377bec91ab86e3c91
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37996087"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workPosition = new WorkPosition
{
    Categories = new List<String>()
    {
        "categories-value"
    },
    Detail = new PositionDetail
    {
        Company = new CompanyDetail
        {
            DisplayName = "displayName-value",
            Pronunciation = "pronunciation-value",
            Department = "department-value",
            OfficeLocation = "officeLocation-value",
            Address = new PhysicalAddress
            {
                Type = PhysicalAddressType.Unknown,
                PostOfficeBox = "postOfficeBox-value",
                Street = "street-value",
                City = "city-value",
                State = "state-value",
                CountryOrRegion = "countryOrRegion-value",
                PostalCode = "postalCode-value"
            },
            WebUrl = "webUrl-value"
        },
        Description = "description-value",
        EndMonthYear = new Date(1900,1,1),
        JobTitle = "jobTitle-value",
        Role = "role-value",
        StartMonthYear = new Date(1900,1,1),
        Summary = "summary-value"
    }
};

await graphClient.Me.Profile.Positions["{id}"]
    .Request()
    .UpdateAsync(workPosition);

```