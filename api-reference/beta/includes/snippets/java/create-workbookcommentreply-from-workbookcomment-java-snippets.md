---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 7912d99a33748fff5dfa51479b65871a62f10913
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48964333"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

WorkbookCommentReply workbookCommentReply = new WorkbookCommentReply();
workbookCommentReply.content = "This is my reply to the comment.";
workbookCommentReply.contentType = "plain";

graphClient.drive().items("{id}").workbook().comments("{id}").replies()
    .buildRequest()
    .post(workbookCommentReply);

```