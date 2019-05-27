---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 5dae900427d3e2b59152efc8d6b5cc3efe4cca5e
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34471042"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var group = await graphClient.Groups["b320ee12-b1cd-4cca-b648-a437be61c5cd"]
    .Request()
    .Select( e => new {
             e.AllowExternalSenders,
             e.AutoSubscribeNewMembers,
             e.IsSubscribedByMail,
             e.UnseenCount 
             })
    .GetAsync();

```