---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 776789492f83c5898520cc7c1e4ac9f20838f3c2
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48621113"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var user = new User
{
    AccountEnabled = true,
    DisplayName = "displayName-value",
    MailNickname = "mailNickname-value",
    UserPrincipalName = "upn-value@tenant-value.onmicrosoft.com",
    PasswordProfile = new PasswordProfile
    {
        ForceChangePasswordNextSignIn = true,
        Password = "password-value"
    }
};

await graphClient.Users
    .Request()
    .AddAsync(user);

```