---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 238fdb9e5304562c887a1c8e8f0fdbbd1ee408c1
ms.sourcegitcommit: 2050639c9e9a6b2dab9ce53d6a9fc87e98789b50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/08/2020
ms.locfileid: "45080834"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var user = new User
{
    DisplayName = "John Smith",
    Identities = new List<ObjectIdentity>()
    {
        new ObjectIdentity
        {
            SignInType = "userName",
            Issuer = "contoso.onmicrosoft.com",
            IssuerAssignedId = "johnsmith"
        },
        new ObjectIdentity
        {
            SignInType = "emailAddress",
            Issuer = "contoso.onmicrosoft.com",
            IssuerAssignedId = "jsmith@yahoo.com"
        },
        new ObjectIdentity
        {
            SignInType = "federated",
            Issuer = "facebook.com",
            IssuerAssignedId = "5eecb0cd"
        }
    },
    PasswordProfile = new PasswordProfile
    {
        Password = "password-value",
        ForceChangePasswordNextSignIn = false
    },
    PasswordPolicies = "DisablePasswordExpiration"
};

await graphClient.Users
    .Request()
    .AddAsync(user);

```