---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a0176e4d9dc5b10f6b75a7a987d16e6f7cc32d54
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35505585"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var acceptedSenders = await graphClient.Groups["{id}"].AcceptedSenders
    .Request()
    .GetAsync();

```