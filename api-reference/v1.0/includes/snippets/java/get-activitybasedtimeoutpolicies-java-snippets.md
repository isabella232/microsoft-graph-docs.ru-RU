---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 6df14537a7fcce0236cf3837a1c12381c6f91a86
ms.sourcegitcommit: 5575e6607817ba23ceb0b01e2f5fc81e58bdcd1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2020
ms.locfileid: "43718497"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IActivityBasedTimeoutPolicyCollectionPage activityBasedTimeoutPolicies = graphClient.policies().activityBasedTimeoutPolicies()
    .buildRequest()
    .get();

```