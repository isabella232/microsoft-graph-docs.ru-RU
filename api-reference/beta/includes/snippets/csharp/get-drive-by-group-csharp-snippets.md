---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 35dc3d56a2e44a371657d36d373bb486ce3b30d1
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35529025"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var drive = await graphClient.Groups["{groupId}"].Drive
    .Request()
    .GetAsync();

```