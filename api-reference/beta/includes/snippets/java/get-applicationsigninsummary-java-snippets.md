---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 55654847595cc0f13d29d19024c318f12264aed9
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35856734"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IApplicationSignInSummaryCollectionPage getAzureADApplicationSignInSummary = graphClient.reports()
    .getAzureADApplicationSignInSummary('D7')
    .buildRequest()
    .get();

```