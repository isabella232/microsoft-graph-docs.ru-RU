---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 30e73bc4e98a181922e013d5b469b54ddad69206
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35871906"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ISkypeForBusinessPeerToPeerActivityUserCountsCollectionPage getSkypeForBusinessPeerToPeerActivityUserCounts = graphClient.reports()
    .getSkypeForBusinessPeerToPeerActivityUserCounts('D7')
    .buildRequest()
    .get();

```