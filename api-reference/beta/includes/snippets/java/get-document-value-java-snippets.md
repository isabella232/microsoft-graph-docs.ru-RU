---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 524e84c1fca81b598c0e5df5284a2035dee79358
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48981503"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

InputStream stream = graphClient.print().printers("fcb0bc53-a446-41d0-bfc3-5c56cdbb0f2a").jobs("46140").documents("bd260b1a-044e-4ca6-afa9-17d9a587d254").content()
    .buildRequest()
    .get();

```