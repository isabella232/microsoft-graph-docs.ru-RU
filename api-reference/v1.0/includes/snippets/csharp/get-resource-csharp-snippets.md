---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 6d9380b5d249aff7a75710f0bb630aecccef71e3
ms.sourcegitcommit: 1585d55d3e7030b5fd1f7cfd5de8f9fb8202cd56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2019
ms.locfileid: "37429215"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var stream = await graphClient.Me.Onenote.Resources["{id}"].Content
    .Request()
    .GetAsync();

```