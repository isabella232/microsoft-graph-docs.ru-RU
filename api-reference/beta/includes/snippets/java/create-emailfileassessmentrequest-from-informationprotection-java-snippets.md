---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 57261ce82734ef49dc61677d47dbcc3bbbdc3b6f
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48952988"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

EmailFileAssessmentRequest threatAssessmentRequest = new EmailFileAssessmentRequest();
threatAssessmentRequest.recipientEmail = "tifc@a830edad9050849EQTPWBJZXODQ.onmicrosoft.com";
threatAssessmentRequest.expectedAssessment = ThreatExpectedAssessment.BLOCK;
threatAssessmentRequest.category = ThreatCategory.MALWARE;
threatAssessmentRequest.contentData = "UmVjZWl2ZWQ6IGZyb20gTVcyUFIwME1CMDMxNC5uYW1wcmQwMC.....";

graphClient.informationProtection().threatAssessmentRequests()
    .buildRequest()
    .post(threatAssessmentRequest);

```