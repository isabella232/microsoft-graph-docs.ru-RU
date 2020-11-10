---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 82673e48d76a8cd6e714c7a09c81b139015d34ac
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48957569"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ConnectedOrganization connectedOrganization = new ConnectedOrganization();
connectedOrganization.displayName = "Connected organization new name";
connectedOrganization.description = "Connected organization new description";
connectedOrganization.state = ConnectedOrganizationState.CONFIGURED;

graphClient.identityGovernance().entitlementManagement().connectedOrganizations("{id}")
    .buildRequest()
    .patch(connectedOrganization);

```