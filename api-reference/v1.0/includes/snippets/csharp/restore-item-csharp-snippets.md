---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: dcec87234c0f12fa61d3c8701151b3d758f993f3
ms.sourcegitcommit: e20c113409836115f338dcfe3162342ef3bd6a4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "45007113"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var parentReference = new ItemReference
{
    Id = "String"
};

var name = "String";

await graphClient.Me.Drive.Items["{item-id}"]
    .Restore(parentReference,name)
    .Request()
    .PostAsync();

```