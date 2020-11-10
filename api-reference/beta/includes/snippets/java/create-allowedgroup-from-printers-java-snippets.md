---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 13e66e6ae48762af646bc8974c69fc013b6228c1
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48967790"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

PrintIdentity printIdentity = new PrintIdentity();
printIdentity.additionalDataManager().put("@odata.id", new JsonPrimitive("https://graph.microsoft.com/beta/groups/{id}"));

graphClient.print().shares("{id}").allowedGroups().references()
    .buildRequest()
    .post(printIdentity);

```