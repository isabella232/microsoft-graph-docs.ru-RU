---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: b347e434bf3500bcc418965cef5de340baf71a3d
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34444596"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupId = "ffffffff-ffff-ffff-ffff-ffffffffffff";

await graphClient.GroupLifecyclePolicies
    .RenewGroup(groupId)
    .Request()
    .PostAsync();

```