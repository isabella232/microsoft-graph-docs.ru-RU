---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 5709bb98d40f0b696796a69e9807afd949b36ec6
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48973776"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

PlannerBucket plannerBucket = new PlannerBucket();
plannerBucket.name = "Advertising";
plannerBucket.planId = "xqQg5FS2LkCp935s-FIFm2QAFkHM";
plannerBucket.orderHint = " !";

graphClient.planner().buckets()
    .buildRequest()
    .post(plannerBucket);

```