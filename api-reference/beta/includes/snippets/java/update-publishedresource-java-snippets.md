---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 3868516361a0f72f32a0112dae2d872015e4fc71
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48973342"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

PublishedResource publishedResource = new PublishedResource();
publishedResource.displayName = "Demo provisioning (updated)";

graphClient.onPremisesPublishingProfiles("provisioning").publishedResources("1234b780-965f-4149-85c5-a8c73e58b67d")
    .buildRequest()
    .patch(publishedResource);

```