---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: bb8263894ca8f83b5fc29d7b34dcfb11287943c9
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2019
ms.locfileid: "37538409"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Users["047dd774-f1c4-40f2-82f0-278de79f9b83"]
    .ReprocessLicenseAssignment()
    .Request()
    .PostAsync();

```