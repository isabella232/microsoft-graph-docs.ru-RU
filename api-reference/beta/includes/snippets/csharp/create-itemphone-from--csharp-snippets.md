---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a99e1e2e1332c5a1c7eba27d0df0d43ca953cccf
ms.sourcegitcommit: 239db9e961e42b505f52de9859963a9136935f2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "46819809"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var itemPhone = new ItemPhone
{
    DisplayName = "Car Phone",
    Number = "+7 499 342 22 13"
};

await graphClient.Me.Profile.Phones
    .Request()
    .AddAsync(itemPhone);

```