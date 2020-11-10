---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f0333c4b33181adceb2406f1ae18768dab6d2b80
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48963430"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Device device = new Device();
device.accountEnabled = true;
LinkedList<AlternativeSecurityId> alternativeSecurityIdsList = new LinkedList<AlternativeSecurityId>();
AlternativeSecurityId alternativeSecurityIds = new AlternativeSecurityId();
alternativeSecurityIds.type = 99;
alternativeSecurityIds.identityProvider = "identityProvider-value";
alternativeSecurityIds.key = Base64.getDecoder().decode("base64Y3YxN2E1MWFlYw==");
alternativeSecurityIdsList.add(alternativeSecurityIds);
device.alternativeSecurityIds = alternativeSecurityIdsList;
device.approximateLastSignInDateTime = CalendarSerializer.deserialize("2016-10-19T10:37:00Z");
device.deviceId = "deviceId-value";
device.deviceMetadata = "deviceMetadata-value";
device.deviceVersion = 99;

graphClient.devices()
    .buildRequest()
    .post(device);

```