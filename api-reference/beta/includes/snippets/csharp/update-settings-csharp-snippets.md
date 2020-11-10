---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a40c2493cdc13b3d175e687d4215393ff688b1d1
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48966949"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var printSettings = new PrintSettings
{
    DocumentConversionEnabled = true
};

var print = new Print();
print.Settings = printSettings;

await graphClient.Print
    .Request()
    .UpdateAsync(print);

```