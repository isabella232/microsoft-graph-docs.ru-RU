---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 9647332c813fa12b69fc3e4b86a9ce44bdffc2d5
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35863874"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

WorkbookChartLineFormat workbookChartLineFormat = graphClient.me().drive().items("{id}").workbook().worksheets("{id|name}").charts("{name}").axes().seriesAxis().format().line()
    .buildRequest()
    .get();

```