---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 39e068b4c0a3cfd5c4ff222350f6b42a255a7208
ms.sourcegitcommit: c0df90d66cb2072848d4bb0bf730c47a601b99ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34546903"
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

var comment = "Please take a look at the attached guidelines before you decide on the name.";

await graphClient.Me.Messages["AAMkADA1MTAAAH5JaKAAA="]
    .ReplyAll(message,comment)
    .Request()
    .PostAsync();

```