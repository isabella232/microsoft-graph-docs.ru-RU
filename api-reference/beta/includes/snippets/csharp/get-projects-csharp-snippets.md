---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 31a10957ab03559dce7401bd10a084a1aed7604b
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "37996881"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var projects = await graphClient.Me.Profile.Projects
    .Request()
    .GetAsync();

```