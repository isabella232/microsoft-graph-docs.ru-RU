---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 5c887a2dcb005c0344cd60ccdc4604d38737d464
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48967474"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

FileAttachment attachment = new FileAttachment();
attachment.name = "smile";
attachment.contentBytes = Base64.getDecoder().decode("a0b1c76de9f7=");

graphClient.me().messages("AAMkpsDRVK").attachments()
    .buildRequest()
    .post(attachment);

```