---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 8ee1a63573c36e8c19d1c5eed770ffd326f0bcd9
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35876330"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

PlannerProgressTaskBoardTaskFormat plannerProgressTaskBoardTaskFormat = graphClient.planner().tasks("'id'").progressTaskBoardFormat()
    .buildRequest()
    .get();

```