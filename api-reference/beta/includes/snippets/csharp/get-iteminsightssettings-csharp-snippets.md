---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ad5986198d06da91e674f3bab0a880f85949ced3
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46569963"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var itemInsightsSettings = await graphClient.Organization["{organizationId}"].Settings.ItemInsights
    .Request()
    .GetAsync();

```