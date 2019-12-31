---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 26e66261b37cc54e8db7abd9b5484d3c23e7aed3
ms.sourcegitcommit: 636671293b0be89088459c4fc8a5e661341b37cf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/31/2019
ms.locfileid: "40911842"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var accessPackageResourceRequest = new AccessPackageResourceRequest
{
    CatalogId = "26ac0c0a-08bc-4a7b-a313-839f58044ba5",
    RequestType = "AdminAdd",
    Justification = "",
    AccessPackageResource = new AccessPackageResource
    {
        DisplayName = "Sales",
        Description = "https://contoso.sharepoint.com/sites/Sales",
        Url = "https://contoso.sharepoint.com/sites/Sales",
        ResourceType = "SharePoint Online Site",
        OriginId = "https://contoso.sharepoint.com/sites/Sales",
        OriginSystem = "SharePointOnline"
    }
};

await graphClient.IdentityGovernance.EntitlementManagement.AccessPackageResourceRequests
    .Request()
    .AddAsync(accessPackageResourceRequest);

```