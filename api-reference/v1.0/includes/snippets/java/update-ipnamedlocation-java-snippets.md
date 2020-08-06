---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 504261a2b758d6c4aa33acd2ff126704c46973cb
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46567370"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IpNamedLocation namedLocation = new IpNamedLocation();
namedLocation.displayName = "Untrusted named location with only IPv4 address";
namedLocation.isTrusted = false;
LinkedList<IpRange> ipRangesList = new LinkedList<IpRange>();
IPv4CidrRange ipRanges = new IPv4CidrRange();
ipRanges.cidrAddress = "6.5.4.3/18";
ipRangesList.add(ipRanges);
namedLocation.ipRanges = ipRangesList;

graphClient.identity().conditionalAccess().namedLocations("0854951d-5fc0-4eb1-b392-9b2c9d7949c2")
    .buildRequest()
    .patch(namedLocation);

```