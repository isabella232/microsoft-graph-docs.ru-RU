---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 0cdd28f4fe188ce9136ea34b91519746f0fc13d7
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "44684618"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var @event = await graphClient.Me.Events["AAMkAGIAAAoZDOFAAA="]
    .Request()
    .Header("Prefer","outlook.timezone=\"Pacific Standard Time\"")
    .Select("subject,body,bodyPreview,organizer,attendees,start,end,location")
    .GetAsync();

```