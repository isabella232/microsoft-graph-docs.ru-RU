---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 9aefec4eed8b697d65f94b80ed46f56de8d0eb3c
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48958899"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

WorkbookChartAxis workbookChartAxis = new WorkbookChartAxis();
JsonElement majorUnit = new JsonObject();
workbookChartAxis.majorUnit = majorUnit;
JsonElement maximum = new JsonObject();
workbookChartAxis.maximum = maximum;
JsonElement minimum = new JsonObject();
workbookChartAxis.minimum = minimum;

graphClient.me().drive().items("{id}").workbook().worksheets("{id|name}").charts("{name}").axes().valueAxis()
    .buildRequest()
    .patch(workbookChartAxis);

```