---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 5bf168a4f16b9c3bf06af4699d03846ab8659366
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35728726"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var Stream = new List<Stream>()
{
    new Stream
    {
        Target = "#para-id",
        Action = "insert",
        Position = "before",
        Content = "<img src=\"image-url-or-part-name\" alt=\"image-alt-text\" />"
    },
    new Stream
    {
        Target = "#list-id",
        Action = "append",
        Content = "<li>new-page-content</li>"
    }
};

var pages = new OnenotePage();
pages.Content = content;

await graphClient.Me.Onenote.Pages["{id}"]
    .Request()
    .UpdateAsync(pages);

```