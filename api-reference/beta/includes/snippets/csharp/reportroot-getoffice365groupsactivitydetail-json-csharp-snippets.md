---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 41c37e9af565248fc85281d5806c839079a735c9
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "36360489"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getOffice365GroupsActivityDetail = await graphClient.Reports
    .GetOffice365GroupsActivityDetail("D7")
    .Request()
    .GetAsync();

```