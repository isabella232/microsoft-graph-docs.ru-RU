---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 2ed3525fc4b27b9fb80a034d5bca73a4c0cfbb8e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496684"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var report = await graphClient.Reports.GetEmailActivityUserCounts('D7')
    .Request()
    .GetAsync();

```