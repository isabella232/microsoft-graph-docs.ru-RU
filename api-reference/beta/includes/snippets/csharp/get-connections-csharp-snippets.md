---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 1151894523cbf9169a00f0618cf36b3859eb17cd
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37994658"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var connections = await graphClient.External.Connections
    .Request()
    .GetAsync();

```