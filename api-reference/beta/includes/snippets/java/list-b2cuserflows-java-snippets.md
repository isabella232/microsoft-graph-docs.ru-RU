---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 86dfac8e96d01c1866a4c7e0582442b615e41530
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48953606"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IB2cIdentityUserFlowCollectionPage b2cUserFlows = graphClient.identity().b2cUserFlows()
    .buildRequest()
    .get();

```