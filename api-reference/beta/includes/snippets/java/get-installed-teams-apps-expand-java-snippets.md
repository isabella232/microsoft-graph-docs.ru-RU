---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 434a0a4a4f2dc71c55ebd1241161db0f18303d15
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48962924"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ITeamsAppInstallationCollectionPage installedApps = graphClient.teams("{id}").installedApps()
    .buildRequest()
    .expand("teamsAppDefinition")
    .get();

```