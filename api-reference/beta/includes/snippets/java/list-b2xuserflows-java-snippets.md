---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 8ce3aa482f894cbbf06fdf371e105e42f5ccb8e4
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48953571"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IB2xIdentityUserFlowCollectionPage b2xUserFlows = graphClient.identity().b2xUserFlows()
    .buildRequest()
    .get();

```