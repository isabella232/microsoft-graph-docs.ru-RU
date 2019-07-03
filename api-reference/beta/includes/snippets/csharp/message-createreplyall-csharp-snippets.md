---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 4813e8297f3832fb6ec9d2196c9f9cf718fc597f
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35529576"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = new Message
{
    Attachments = new List<Attachment>()
    {
        new Attachment
        {
            Name = "guidelines.txt",
            ContentBytes = "bWFjIGFuZCBjaGVlc2UgdG9kYXk="
        }
    }
};

var comment = "if the project gets approved, please take a look at the attached guidelines before you decide on the name.";

await graphClient.Me.Messages["AAMkADA1MTAAAH5JaKAAA="]
    .CreateReplyAll(message,comment)
    .Request()
    .PostAsync();

```