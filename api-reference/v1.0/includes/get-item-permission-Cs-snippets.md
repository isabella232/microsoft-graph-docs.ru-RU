---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 82d8a96c21aae5396d2e8339429f7e57bae8cf09
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34454848"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var permission = await graphClient.Me.Drive.Items["{item-id}"].Permissions["{perm-id}"]
    .Request()
    .GetAsync();

```