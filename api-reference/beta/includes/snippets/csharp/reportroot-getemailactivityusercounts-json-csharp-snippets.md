---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 4adc358ec9cd447247aafb2eca8b2b3c828b626c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35529630"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getEmailActivityUserCounts = await graphClient.Reports.GetEmailActivityUserCounts('D7')
    .Request()
    .GetAsync();

```