---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 48e342a14d69a79e615680d0b28e5b85a2b9d087
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "44684850"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var mailFolder = new MailSearchFolder
{
    DisplayName = "Weekly digests",
    IncludeNestedFolders = true,
    SourceFolderIds = new List<String>()
    {
        "AQMkADYAAAIBDAAAAA=="
    },
    FilterQuery = "contains(subject, 'weekly digest')"
};

await graphClient.Me.MailFolders["AQMkADYAAAIBDAAAAA=="].ChildFolders
    .Request()
    .AddAsync(mailFolder);

```