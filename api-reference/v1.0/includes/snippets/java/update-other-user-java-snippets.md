---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 7e28bf999ad98c2fcd5d04f9dc791906878d27dd
ms.sourcegitcommit: 3db93e28e215c0e09a65b4705ba956c6ac3b5426
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/14/2019
ms.locfileid: "36396844"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

User user = new User();
LinkedList<String> businessPhonesList = new LinkedList<String>();
businessPhonesList.add("businessPhones-value");
user.businessPhones = businessPhonesList;
user.officeLocation = "city-value";

graphClient.users("{id}")
    .buildRequest()
    .patch(user);

```