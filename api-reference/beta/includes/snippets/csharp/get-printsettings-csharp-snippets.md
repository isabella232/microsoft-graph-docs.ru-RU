---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 766ef355895177ba7ef68f96c2d1d2ec388e8834
ms.sourcegitcommit: 33ffed5b785abf36b1a7786856c9266958830d25
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2020
ms.locfileid: "42948361"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var print = await graphClient.Print
    .Request()
    .Select( e => new {
             e.Settings 
             })
    .GetAsync();

var settings = print.Settings;

```