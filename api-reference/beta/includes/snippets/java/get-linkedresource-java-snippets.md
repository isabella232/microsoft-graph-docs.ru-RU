---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 07c790c74f7d16f519d300cbf30007aca4e6c67e
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48974379"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ILinkedResourceCollectionPage linkedResources = graphClient.me().todo().lists("dfsdc-f9dfdfs-dcsda9").tasks("e2dc-f9cce2-dce29").linkedResources()
    .buildRequest()
    .get();

```