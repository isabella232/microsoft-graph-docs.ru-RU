---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 620219473eae66c7f219e2ba44d263fefd38aa5d
ms.sourcegitcommit: ef8eac3cf973a1971f8f1d41d75a085fad3690f0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2019
ms.locfileid: "37997064"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var place = new Roomlist
{
    DisplayName = "Building 1",
    Phone = "555-555-0100"
};

await graphClient.Places["Building1RroomList@contoso.onmicrosoft.com"]
    .Request()
    .UpdateAsync(place);

```