---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 29203eb354bf5bef9492c69ac457b36aaa020e29
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35861832"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IDomainDnsRecordCollectionPage serviceConfigurationRecords = graphClient.domains("contoso.com").serviceConfigurationRecords()
    .buildRequest()
    .get();

```