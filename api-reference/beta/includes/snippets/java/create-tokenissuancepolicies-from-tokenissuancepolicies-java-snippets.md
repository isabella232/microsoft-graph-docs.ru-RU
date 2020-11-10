---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 811f8ac04c789f05ee995d9dc6e288d3910aff90
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48980257"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

TokenIssuancePolicy tokenIssuancePolicy = new TokenIssuancePolicy();
LinkedList<String> definitionList = new LinkedList<String>();
definitionList.add("definition-value");
tokenIssuancePolicy.definition = definitionList;
tokenIssuancePolicy.displayName = "displayName-value";
tokenIssuancePolicy.isOrganizationDefault = true;

graphClient.policies().tokenIssuancePolicies()
    .buildRequest()
    .post(tokenIssuancePolicy);

```