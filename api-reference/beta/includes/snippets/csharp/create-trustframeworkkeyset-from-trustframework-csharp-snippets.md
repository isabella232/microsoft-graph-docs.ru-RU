---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 48ab8807142244a550cf57bf7c56ad862118741d
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "37938320"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var trustFrameworkKeySet = new TrustFrameworkKeySet
{
    Id = "keyset1",
    Keys = new List<TrustFrameworkKey>()
    {
        new TrustFrameworkKey
        {
            K = "k-value",
            X5c = new List<String>()
            {
                "x5c-value"
            },
            X5t = "x5t-value",
            Kty = "kty-value",
            Use = "use-value",
            Exp = 99,
            Nbf = 99,
            Kid = "kid-value",
            E = "e-value",
            N = "n-value",
            D = "d-value",
            P = "p-value",
            Q = "q-value",
            Dp = "dp-value",
            Dq = "dq-value",
            Qi = "qi-value"
        }
    }
};

await graphClient.TrustFramework.KeySets
    .Request()
    .AddAsync(trustFrameworkKeySet);

```