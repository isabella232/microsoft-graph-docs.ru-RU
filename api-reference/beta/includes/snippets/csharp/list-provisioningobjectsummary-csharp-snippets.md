---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: ffc7dff41d0baf03830ce84737dfe9c8643685a7
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35720015"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var directoryProvisioning = await graphClient.AuditLogs.DirectoryProvisioning
    .Request()
    .GetAsync();

```