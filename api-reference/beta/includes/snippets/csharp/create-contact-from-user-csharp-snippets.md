---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 588f5fd28ad7c86554b0167b8d7ef279689cc5fa
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48618490"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var contact = new Contact
{
    GivenName = "Pavel",
    Surname = "Bansky",
    EmailAddresses = new List<TypedEmailAddress>()
    {
        new TypedEmailAddress
        {
            Address = "pavelb@contoso.onmicrosoft.com",
            Name = "Pavel Bansky",
            Type = EmailType.Personal
        },
        new TypedEmailAddress
        {
            Address = "pavelb@fabrikam.onmicrosoft.com",
            Name = "Pavel Bansky",
            Type = EmailType.Other,
            OtherLabel = "Volunteer work"
        }
    },
    Phones = new List<Phone>()
    {
        new Phone
        {
            Number = "+1 732 555 0102",
            Type = PhoneType.Business
        }
    }
};

await graphClient.Me.Contacts
    .Request()
    .AddAsync(contact);

```