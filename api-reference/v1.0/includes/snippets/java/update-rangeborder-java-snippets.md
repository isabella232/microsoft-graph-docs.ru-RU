---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 1a2aa3cb811ebe519c97c9bbc30d4e624a9dadd7
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35889889"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

WorkbookRangeBorder workbookRangeBorder = new WorkbookRangeBorder();
workbookRangeBorder.color = "color-value";
workbookRangeBorder.style = "style-value";
workbookRangeBorder.sideIndex = "sideIndex-value";
workbookRangeBorder.weight = "weight-value";

graphClient.me().drive().items("{id}").workbook().names("{name}")
    .range().format().borders("{sideIndex}")
    .buildRequest()
    .patch(workbookRangeBorder);

```