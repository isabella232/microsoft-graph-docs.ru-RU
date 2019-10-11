---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 334970957145172050de54f44961f28aba7ecdad
ms.sourcegitcommit: 1585d55d3e7030b5fd1f7cfd5de8f9fb8202cd56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2019
ms.locfileid: "37429140"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var stream = new List<Stream>()
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

await graphClient.Me.Onenote.Pages["{id}"].Content
    .Request()
    .UpdateAsync(pages);

```