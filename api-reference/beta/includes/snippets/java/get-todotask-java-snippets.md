---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 5da2e9bc625f99b8110629ab3671ecc7a3004b6d
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48972529"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ITodoTaskCollectionPage tasks = graphClient.me().todo().lists("35e2-35e2-721a-e235-1a72e2351a7").tasks()
    .buildRequest()
    .get();

```