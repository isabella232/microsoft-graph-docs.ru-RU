---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f1795572ecdfa9e185dee24715a9ec89945fb13a
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34445100"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var verificationDnsRecords = await graphClient.Domains["contoso.com"].VerificationDnsRecords
    .Request()
    .GetAsync();

```