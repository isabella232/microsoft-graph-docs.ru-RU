---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ddfeab2fedceab3583b41ae5e7070c8ec5fb1d93
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48971592"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LanguageProficiency languageProficiency = new LanguageProficiency();
languageProficiency.allowedAudiences = EnumSet.of(AllowedAudiences.ORGANIZATION);

graphClient.me().profile().languages("{id}")
    .buildRequest()
    .patch(languageProficiency);

```