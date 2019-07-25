---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 8a9c9801ea7f913740106403abccff7c045daae6
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35877680"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Attachment attachment = new Attachment();
attachment.lastModifiedDateTime = "datetime-value";
attachment.name = "name-value";
attachment.contentType = "contentType-value";
attachment.size = 99;
attachment.isInline = true;

graphClient.users("{id}").outlook().tasks("{id}").attachments()
    .buildRequest()
    .post(attachment);

```