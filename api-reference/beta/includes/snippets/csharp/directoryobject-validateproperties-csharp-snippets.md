---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: afc05efa66a2fc3de78f5193288440d696c3eeee
ms.sourcegitcommit: d8a58221ed1f2b7b7073fd621da4737e11ba53c5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/11/2019
ms.locfileid: "36846160"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var entityType = "Group";

var displayName = "Myprefix_test_mysuffix";

var mailNickname = "Myprefix_test_mysuffix";

var onBehalfOfUserId = Guid.Parse("onBehalfOfUserId-value");

await graphClient.DirectoryObjects
    .ValidateProperties(entityType,displayName,mailNickname,onBehalfOfUserId)
    .Request()
    .PostAsync();

```