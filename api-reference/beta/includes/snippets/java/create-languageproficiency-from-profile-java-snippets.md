---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 454be4e5d8e512410b427595d7aa74c86624aa82
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48979592"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LanguageProficiency languageProficiency = new LanguageProficiency();
languageProficiency.displayName = "Norwegian Bokmål";
languageProficiency.tag = "nb-NO";
languageProficiency.spoken = LanguageProficiencyLevel.NATIVE_OR_BILINGUAL;
languageProficiency.written = LanguageProficiencyLevel.NATIVE_OR_BILINGUAL;
languageProficiency.reading = LanguageProficiencyLevel.NATIVE_OR_BILINGUAL;

graphClient.me().profile().languages()
    .buildRequest()
    .post(languageProficiency);

```