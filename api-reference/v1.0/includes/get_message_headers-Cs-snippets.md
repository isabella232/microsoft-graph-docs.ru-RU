---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f4857e5e52c2cb2f27cff8dbc7438e4884a3b6f0
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34461088"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = await graphClient.Me.Messages["AAMkADhAAAW-VPeAAA="]
    .Request()
    .Select( e => new {
             e.InternetMessageHeaders 
             })
    .GetAsync();

```