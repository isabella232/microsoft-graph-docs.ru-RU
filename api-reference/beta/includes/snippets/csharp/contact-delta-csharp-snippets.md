---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f3379b2ab6ebbc7aa99a7cece00d2dbeb5c18e4c
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "44685234"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var delta = await graphClient.Me.ContactFolders["{id}"].Contacts
    .Delta()
    .Request()
    .Select("displayName")
    .GetAsync();

```