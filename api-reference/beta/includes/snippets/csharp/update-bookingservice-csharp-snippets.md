---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 55f7725ffe62e428b0ed38ceeb0683224888745c
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35865274"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var bookingService = new BookingService
{
    AdditionalData = new Dictionary<string, object>()
    {
        {"@odata.type","#microsoft.graph.bookingService"}
    },
    DefaultDuration = "PT30M"
};

await graphClient.BookingBusinesses["Contosolunchdelivery@M365B489948.onmicrosoft.com"].Services["57da6774-a087-4d69-b0e6-6fb82c339976"]
    .Request()
    .UpdateAsync(bookingService);

```