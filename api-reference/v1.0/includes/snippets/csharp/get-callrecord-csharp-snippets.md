---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 5db6923a49454290f96e123da14ce81d28747ae5
ms.sourcegitcommit: 43f7800894857a29f02fffaf4a50ad6386b5bf59
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2020
ms.locfileid: "44524670"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var callRecord = await graphClient.Communications.CallRecords["{id}"]
    .Request()
    .GetAsync();

```