---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 213479637477d1a48f3c1c74aace7746336cd63f
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48977541"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String calculationType = "calculationType-value";

graphClient.me().drive().items("{id}").workbook().application()
    .calculate(calculationType)
    .buildRequest()
    .post();

```