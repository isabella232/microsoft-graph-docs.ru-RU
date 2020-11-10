---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: c17ed789e4742c08287a9b44d5dfefbe24eb3c8d
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48980013"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<String> inputIdsList = new LinkedList<String>();
inputIdsList.add("{rest-formatted-id-1}");
inputIdsList.add("{rest-formatted-id-2}");

ExchangeIdFormat sourceIdType = ExchangeIdFormat.REST_ID;

ExchangeIdFormat targetIdType = ExchangeIdFormat.REST_IMMUTABLE_ENTRY_ID;

graphClient.me()
    .translateExchangeIds(inputIdsList,targetIdType,sourceIdType)
    .buildRequest()
    .post();

```