---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 15738081d83480599c650c9708b481e56100c5cf
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48957309"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Connector connector = new Connector();
connector.additionalDataManager().put("@odata.id", new JsonPrimitive("https://graph.microsoft.com/beta/onPremisesPublishingProfiles/applicationProxy/connectors/{id}"));

graphClient.onPremisesPublishingProfiles("applicationProxy").connectorGroups("{id}").members().references()
    .buildRequest()
    .post(connector);

```