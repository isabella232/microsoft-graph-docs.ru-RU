---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 668dd8b1a440b3a2d9e59df6fc41ac0b85ff80ae
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35718259"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var schedule = await graphClient.Teams["{teamId}"].Schedule
    .Request()
    .GetAsync();

```