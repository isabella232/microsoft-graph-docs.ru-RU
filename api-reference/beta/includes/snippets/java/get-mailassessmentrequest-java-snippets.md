---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d78a78c0f57247012c18abae2dbb5de84ed942dd
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48977877"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ThreatAssessmentRequest threatAssessmentRequest = graphClient.informationProtection().threatAssessmentRequests("49c5ef5b-1f65-444a-e6b9-08d772ea2059")
    .buildRequest()
    .get();

```