---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 0d376d2aa02ee7d52b6ccbb45ddeaba572cddfb3
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46567110"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

CountryNamedLocation namedLocation = new CountryNamedLocation();
namedLocation.displayName = "Updated named location without unknown countries and regions";
LinkedList<String> countriesAndRegionsList = new LinkedList<String>();
countriesAndRegionsList.add("CA");
countriesAndRegionsList.add("IN");
namedLocation.countriesAndRegions = countriesAndRegionsList;
namedLocation.includeUnknownCountriesAndRegions = false;

graphClient.identity().conditionalAccess().namedLocations("1c4427fd-0885-4a3d-8b23-09a899ffa959")
    .buildRequest()
    .patch(namedLocation);

```