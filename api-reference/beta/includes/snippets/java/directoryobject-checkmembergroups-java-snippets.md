---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 3870e2e7d47512953e084482810559d3c85617a3
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48963129"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<String> groupIdsList = new LinkedList<String>();
groupIdsList.add("fee2c45b-915a-4a64-b130-f4eb9e75525e");
groupIdsList.add("4fe90ae7-065a-478b-9400-e0a0e1cbd540");

graphClient.me()
    .checkMemberGroups(groupIdsList)
    .buildRequest()
    .post();

```