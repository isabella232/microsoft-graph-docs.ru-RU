---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 6ad96a4a9d97a4a2ff690fb880c01331369a3f87
ms.sourcegitcommit: 46ee19b244349e2a1537f0c44c576d7c01cf03a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/05/2019
ms.locfileid: "37402853"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String comment = "comment-value";

boolean sendResponse = true;

graphClient.me().events("{id}")
    .decline(sendResponse,comment)
    .buildRequest()
    .post();

```