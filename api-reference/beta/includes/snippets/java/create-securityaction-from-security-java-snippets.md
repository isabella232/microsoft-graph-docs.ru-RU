---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 39ec9865f613bccce16a21f8128ae5126ad16574
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48970919"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

SecurityAction securityAction = new SecurityAction();
securityAction.name = "BlockIp";
securityAction.actionReason = "Test";
LinkedList<KeyValuePair> parametersList = new LinkedList<KeyValuePair>();
KeyValuePair parameters = new KeyValuePair();
parameters.name = "IP";
parameters.value = "1.2.3.4";
parametersList.add(parameters);
securityAction.parameters = parametersList;
SecurityVendorInformation vendorInformation = new SecurityVendorInformation();
vendorInformation.provider = "Windows Defender ATP";
vendorInformation.vendor = "Microsoft";
securityAction.vendorInformation = vendorInformation;

graphClient.security().securityActions()
    .buildRequest()
    .post(securityAction);

```