---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 4578139588d3203f9e6f0b5c63cefedd9311d12d
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48612431"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var governanceRoleSetting = await graphClient.PrivilegedAccess["azureResources"].RoleSettings["80dc5d6f-8d89-47b3-953f-01dc909ed3f9"]
    .Request()
    .GetAsync();

```