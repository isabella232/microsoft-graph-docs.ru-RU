---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 4a7367dd63b34c9c530ed27985cfa1cb7335fdfa
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34440095"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var outlookTaskFolder = new OutlookTaskFolder
{
    Name = "Volunteer"
};

await graphClient.Me.Outlook.TaskFolders
    .Request()
    .AddAsync(outlookTaskFolder);

```