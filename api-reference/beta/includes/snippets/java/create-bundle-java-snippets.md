---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 9265662ccf1939a3596113c511d7da5d72509b69
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48955784"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

DriveItem driveItem = new DriveItem();
driveItem.name = "Just some files";
driveItem.additionalDataManager().put("@microsoft.graph.conflictBehavior", new JsonPrimitive("rename"));
Bundle bundle = new Bundle();
driveItem.bundle = bundle;
LinkedList<DriveItem> childrenList = new LinkedList<DriveItem>();
DriveItem children = new DriveItem();
children.id = "1234asdf";
childrenList.add(children);
DriveItem children1 = new DriveItem();
children1.id = "1234qwerty";
childrenList.add(children1);
DriveItemCollectionResponse driveItemCollectionResponse = new DriveItemCollectionResponse();
driveItemCollectionResponse.value = childrenList;
DriveItemCollectionPage driveItemCollectionPage = new DriveItemCollectionPage(driveItemCollectionResponse, null);
driveItem.children = driveItemCollectionPage;

graphClient.drive().bundles()
    .buildRequest()
    .post(driveItem);

```