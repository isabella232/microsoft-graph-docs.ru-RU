---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 8d5e88b8a65a35e21615eba492ad5cb6b6e5c1a2
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34466290"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var schemaExtensions = await graphClient.SchemaExtensions
    .Request()
    .Filter("id eq 'graphlearn_test'")
    .GetAsync();

```