---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 319872d786635e26036c73ac3c8c230842defcb2
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48981111"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IUnifiedRoleDefinitionCollectionPage roleDefinitions = graphClient.roleManagement().directory().roleDefinitions()
    .buildRequest()
    .get();

```