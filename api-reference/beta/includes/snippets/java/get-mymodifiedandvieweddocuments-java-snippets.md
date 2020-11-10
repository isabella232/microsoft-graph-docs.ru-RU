---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 52fa13dbc6422c5638c99fd03fb6e3fb0647fcab
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48964618"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IUsedInsightCollectionPage used = graphClient.me().insights().used()
    .buildRequest()
    .orderBy("LastUsed/LastAccessedDateTime desc")
    .get();

```