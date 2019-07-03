---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: b9327c09f777a844b5ef86804b68624d6e3a963a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35506066"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var bookingCustomer = new BookingCustomer
{
    DisplayName = "Adele",
    EmailAddress = "adele@relecloud.com"
};

await graphClient.BookingBusinesses["Contosolunchdelivery@M365B489948.onmicrosoft.com"].Customers["8bb19078-0f45-4efb-b2c5-da78b860f73a"]
    .Request()
    .UpdateAsync(bookingCustomer);

```