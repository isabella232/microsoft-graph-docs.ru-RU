---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d9c57eb3de9ff3640276d79ea877af01f2895ac7
ms.sourcegitcommit: f50b1feff72182d1e19bfa346304beaf29558b68
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2019
ms.locfileid: "36464970"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var clientContext = "fd1c7836-4d84-4e24-b6aa-23188688cc54";

await graphClient.App.Calls["{id}"]
    .SubscribeToTone(clientContext)
    .Request()
    .PostAsync();

```