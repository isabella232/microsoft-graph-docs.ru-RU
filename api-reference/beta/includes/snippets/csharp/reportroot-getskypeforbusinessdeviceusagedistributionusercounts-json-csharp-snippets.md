---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 30f09cbea35f1d93979a02dc277a663b9a1ebb27
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35872397"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getSkypeForBusinessDeviceUsageDistributionUserCounts = await graphClient.Reports
    .GetSkypeForBusinessDeviceUsageDistributionUserCounts('D7')
    .Request()
    .GetAsync();

```