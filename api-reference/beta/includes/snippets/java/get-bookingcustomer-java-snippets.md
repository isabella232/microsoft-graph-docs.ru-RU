---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 3f146d10c709a3e3bbbca3830af1541d317786e0
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48960494"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

BookingCustomer bookingCustomer = graphClient.bookingBusinesses("Contosolunchdelivery@M365B489948.onmicrosoft.com").customers("8bb19078-0f45-4efb-b2c5-da78b860f73a")
    .buildRequest()
    .get();

```