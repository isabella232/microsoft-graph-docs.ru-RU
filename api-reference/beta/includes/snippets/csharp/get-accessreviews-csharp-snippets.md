---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 983054e504cf7b31ebf3af73b13dbe17d5385209
ms.sourcegitcommit: 0329bbcd5f1b09a2a6c5f935a30c4560b6eed492
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "36633267"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var accessReviews = await graphClient.AccessReviews
    .Request()
    .Filter("businessFlowTemplateId+eq+'6E4F3D20-C5C3-407F-9695-8460952BCC68'")
    .GetAsync();

```