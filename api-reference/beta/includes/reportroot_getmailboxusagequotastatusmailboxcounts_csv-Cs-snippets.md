---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 469c0ce2e847181b58b3205b6209724fa5d1a066
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34441957"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getMailboxUsageQuotaStatusMailboxCounts = await graphClient.Reports.GetMailboxUsageQuotaStatusMailboxCounts('D7')
    .Request()
    .GetAsync();

```