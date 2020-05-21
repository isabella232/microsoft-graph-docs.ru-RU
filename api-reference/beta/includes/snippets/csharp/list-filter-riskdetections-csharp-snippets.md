---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: b94efb99bb4409c635ecac9520eccffe8f029db0
ms.sourcegitcommit: 5a1373f2ccd9ee813fc60d42e7ac6b115b5f9f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "44338978"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var riskDetections = await graphClient.RiskDetections
    .Request()
    .Filter("riskEventType eq 'unfamiliarFeatures' or riskLevel eq 'medium'")
    .GetAsync();

```