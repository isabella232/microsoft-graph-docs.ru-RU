---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 51556a7c98ff5e862cb9d303e88a3a5255ab58b6
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35869188"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IAttributeMappingFunctionSchemaCollectionPage functions = graphClient.servicePrincipals("{id}").synchronization().jobs("{jobId}").schema()
    .functions()
    .buildRequest()
    .get();

```