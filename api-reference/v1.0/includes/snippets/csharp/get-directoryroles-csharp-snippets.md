---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 80be132d0345accb780d2c9c1ddee8a6d9b9fb4e
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48621257"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var directoryRoles = await graphClient.DirectoryRoles
    .Request()
    .GetAsync();

```