---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 501b58065032f187538735e84127fc2009c1219b
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35864030"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

WorkbookChartFont workbookChartFont = graphClient.me().drive().items("{id}").workbook().worksheets("{id|name}").charts("{name}").axes().valueAxis().format().font()
    .buildRequest()
    .get();

```