---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: b9b671c54cb24e0a681111950c1c61fb2231e61b
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35872327"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ISkypeForBusinessDeviceUsageUserDetailCollectionPage getSkypeForBusinessDeviceUsageUserDetail = graphClient.reports()
    .getSkypeForBusinessDeviceUsageUserDetail('D7')
    .buildRequest()
    .get();

```