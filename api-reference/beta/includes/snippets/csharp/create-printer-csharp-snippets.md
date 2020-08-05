---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ffe034b1357284edd9e4515a4450af48bfd62d69
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46566371"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var displayName = "Test Printer";

var manufacturer = "Test Printer Manufacturer";

var model = "Test Printer Model";

var physicalDeviceId = null;

var hasPhysicalDevice = false;

var certificateSigningRequest = new PrintCertificateSigningRequestObject
{
    Content = "{content}",
    TransportKey = "{sampleTransportKey}"
};

var connectorId = null;

await graphClient.Print.Printers
    .Create(displayName,manufacturer,model,certificateSigningRequest,physicalDeviceId,hasPhysicalDevice,connectorId)
    .Request()
    .PostAsync();

```