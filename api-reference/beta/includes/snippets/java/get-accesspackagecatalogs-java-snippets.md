---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: e1ff1d5b3d5fa2e467db49eba2ab0586ece14305
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48951920"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IAccessPackageCatalogCollectionPage accessPackageCatalogs = graphClient.identityGovernance().entitlementManagement().accessPackageCatalogs()
    .buildRequest()
    .get();

```