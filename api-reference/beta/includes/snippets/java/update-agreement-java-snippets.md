---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d9930f33d83ee691aa39d77ab97950e95b11e4ae
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48962423"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Agreement agreement = new Agreement();
agreement.displayName = "displayName-value";
agreement.isViewingBeforeAcceptanceRequired = true;

graphClient.agreements("{id}")
    .buildRequest()
    .patch(agreement);

```