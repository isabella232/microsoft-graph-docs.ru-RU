---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: dfa3b7c1b32edf85835ef3ae19ea0c931ad0b01f
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34464470"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getSkypeForBusinessDeviceUsageDistributionUserCounts = await graphClient.Reports.GetSkypeForBusinessDeviceUsageDistributionUserCounts('D7')
    .Request()
    .GetAsync();

```