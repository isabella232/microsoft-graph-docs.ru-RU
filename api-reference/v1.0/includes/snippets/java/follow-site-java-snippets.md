---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 923ae4baac426bd32a640167efe1fe058cb74521
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48982949"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<Site> valueList = new LinkedList<Site>();
Site value = new Site();
value.id = "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,712a596e-90a1-49e3-9b48-bfa80bee8740";

valueList.add(value);
Site value1 = new Site();
value1.id = "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,0271110f-634f-4300-a841-3a8a2e851851";

valueList.add(value1);
SiteCollectionResponse siteCollectionResponse = new SiteCollectionResponse();
siteCollectionResponse.value = valueList;
SiteCollectionPage siteCollectionPage = new SiteCollectionPage(siteCollectionResponse, null);

graphClient.users("{user-id}").followedSites()
    .add(valueList)
    .buildRequest()
    .post();

```