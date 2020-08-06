---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 2da7fa557fa6b6e9cf6a6e677bc98addf5595316
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46566012"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

CountryNamedLocation namedLocation = new CountryNamedLocation();
namedLocation.displayName = "Named location with unknown countries and regions";
LinkedList<String> countriesAndRegionsList = new LinkedList<String>();
countriesAndRegionsList.add("US");
countriesAndRegionsList.add("GB");
namedLocation.countriesAndRegions = countriesAndRegionsList;
namedLocation.includeUnknownCountriesAndRegions = true;

graphClient.identity().conditionalAccess().namedLocations()
    .buildRequest()
    .post(namedLocation);

```