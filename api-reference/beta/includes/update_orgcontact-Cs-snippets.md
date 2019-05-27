---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 01fdff3219a393e9752e7f388e779d2922ffeecd
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34460624"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var orgContact = new OrgContact
{
    BusinessPhones = new List<String>()
    {
        "businessPhones-value"
    },
    City = "city-value",
    CompanyName = "companyName-value",
    Country = "country-value",
    Department = "department-value",
    DisplayName = "displayName-value"
};

await graphClient.Contacts["{id}"]
    .Request()
    .UpdateAsync(orgContact);

```