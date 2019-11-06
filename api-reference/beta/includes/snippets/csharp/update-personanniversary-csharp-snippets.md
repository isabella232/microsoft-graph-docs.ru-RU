---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 0f7a20b8363dbf20df0067bc0887e907ce2d8167
ms.sourcegitcommit: 60dfb2ad9ef17f2918c4ee34ebb74f63e32ce2d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "37997283"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var personAnniversary = new PersonAnniversary
{
    Type = AnniversaryType.Birthday,
    Date = new Date(1900,1,1)
};

await graphClient.Me.Profile.Anniversaries["{id}"]
    .Request()
    .UpdateAsync(personAnniversary);

```