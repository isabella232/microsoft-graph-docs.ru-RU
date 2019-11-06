---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a646c71de8cd8f0b0f1cafc986c959c30a5b3baf
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37994202"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var accessPackage = await graphClient.IdentityGovernance.EntitlementManagement.AccessPackages["{id}"]
    .Request()
    .Expand("accessPackageResourceRoleScopes($expand=accessPackageResourceRole,accessPackageResourceScope)")
    .GetAsync();

```