---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 5d3f9f8f4b670bc4cd44b86437b4c844d999c645
ms.sourcegitcommit: 33ffed5b785abf36b1a7786856c9266958830d25
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2020
ms.locfileid: "42947674"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var printerShare = await graphClient.Print.PrinterShares["{id}"]
    .Request()
    .GetAsync();

```