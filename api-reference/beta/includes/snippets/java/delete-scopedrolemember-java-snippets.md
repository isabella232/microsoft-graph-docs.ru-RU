---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 3c775c40d8e18f27ccc8510d51e01d5b37952360
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48962723"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

graphClient.administrativeUnits("{id}").scopedRoleMembers("{id}")
    .buildRequest()
    .delete();

```