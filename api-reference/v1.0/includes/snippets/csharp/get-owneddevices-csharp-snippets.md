---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d1806b82098ee9d08f5bea3afe79f1d72a94256f
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35515278"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var ownedDevices = await graphClient.Me.OwnedDevices
    .Request()
    .GetAsync();

```