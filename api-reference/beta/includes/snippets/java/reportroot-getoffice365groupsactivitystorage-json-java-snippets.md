---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 689b78ad1c97d65c555ff9357f97c2425a541af7
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35873280"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IOffice365GroupsActivityStorageCollectionPage getOffice365GroupsActivityStorage = graphClient.reports()
    .getOffice365GroupsActivityStorage('D7')
    .buildRequest()
    .get();

```