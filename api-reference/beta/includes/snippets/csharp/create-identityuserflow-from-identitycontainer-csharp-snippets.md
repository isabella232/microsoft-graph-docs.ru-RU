---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: e652e6965d68c206f7a8d992b85142fdfb451d6d
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "37938573"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var identityUserFlow = new IdentityUserFlow
{
    UserFlowType = UserFlowType.SignUpOrSignIn,
    UserFlowTypeVersion = 1
};

await graphClient.Identity.UserFlows
    .Request()
    .AddAsync(identityUserFlow);

```