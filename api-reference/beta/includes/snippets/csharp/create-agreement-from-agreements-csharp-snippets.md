---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 70f84d67f9406af7823b6d4230692eb5701a8da0
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "44684766"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var agreement = new Agreement
{
    DisplayName = "MSGraph Sample",
    IsViewingBeforeAcceptanceRequired = true,
    Files = (IAgreementFilesCollectionPage)new List<AgreementFile>()
    {
        new AgreementFile
        {
            FileName = "TOU.pdf",
            Language = "en",
            IsDefault = true,
            FileData = new AgreementFileData
            {
                Data = Encoding.ASCII.GetBytes("SGVsbG8gd29ybGQ=")
            }
        }
    }
};

await graphClient.Agreements
    .Request()
    .AddAsync(agreement);

```