---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 3967e90761b9a10a1025baa594e9426bd443efc3
ms.sourcegitcommit: 01f73b4dce6f885da18d62fe800b387c286c7a8e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "47413362"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Group group = new Group();
group.additionalDataManager().put("members@odata.bind", new JsonPrimitive("[
  "https://graph.microsoft.com/v1.0/directoryObjects/{id}",
  "https://graph.microsoft.com/v1.0/directoryObjects/{id}",
  "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
]"));

graphClient.groups("{group-id}")
    .buildRequest()
    .patch(group);

```