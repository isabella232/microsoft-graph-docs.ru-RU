---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: af89914b72814d21a91d3740df539cc091ed9483
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48967559"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IOAuth2PermissionGrantCollectionPage oauth2PermissionGrants = graphClient.oauth2PermissionGrants()
    .buildRequest()
    .get();

```