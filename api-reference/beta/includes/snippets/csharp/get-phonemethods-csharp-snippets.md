---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f0a39e6ef9e226738574bdb96e4e2c132305e400
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2020
ms.locfileid: "43805825"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var phoneMethods = await graphClient.Me.Authentication.PhoneMethods
    .Request()
    .GetAsync();

```