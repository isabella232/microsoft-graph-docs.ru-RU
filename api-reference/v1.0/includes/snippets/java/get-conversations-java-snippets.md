---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: cd5b6b5888aebbf6c59a271620b1938ecce873f9
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35889232"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IConversationCollectionPage conversations = graphClient.groups("{id}").conversations()
    .buildRequest()
    .get();

```