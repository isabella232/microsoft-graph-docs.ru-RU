---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 8a496b70ecc5792b8fe2688467ab4ea50938640c
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48980622"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IAppRoleAssignmentCollectionPage appRoleAssignments = graphClient.servicePrincipals("{id}").appRoleAssignments()
    .buildRequest()
    .get();

```