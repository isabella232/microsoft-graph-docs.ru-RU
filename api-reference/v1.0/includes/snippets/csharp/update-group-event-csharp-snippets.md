---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: fdf7267983b422bb3000cc29628f4116a603d6dc
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48607414"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var @event = new Event
{
    Location = new Location
    {
        DisplayName = "Conf Room 2"
    }
};

await graphClient.Groups["01d4ee64-15ce-491e-bad1-b91aa3223df4"].Calendar.Events["AAMkADZlAAAAABERAAA="]
    .Request()
    .UpdateAsync(@event);

```