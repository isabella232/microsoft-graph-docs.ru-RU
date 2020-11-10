---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f76a9ca13b60fb2cdb839637b6a8bc1107a4601b
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48961058"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IdentityProvider identityProviders = new IdentityProvider();
identityProviders.additionalDataManager().put("@odata.id", new JsonPrimitive("https://graph.microsoft.com/beta/identityProviders/{id}"));

graphClient.identity().b2xUserFlows("{id}").identityProviders().references()
    .buildRequest()
    .patch(identityProviders);

```