---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 2adb3194f88ed62d8ce501b4676efef31a21e400
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "37637848"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var tasks = await graphClient.Planner.Plans["{plan-id}"].Tasks
    .Request()
    .GetAsync();

```