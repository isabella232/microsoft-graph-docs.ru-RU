---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 100d37e2882d45041abd66a015630b721243a262
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48983291"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

INotebookGetRecentNotebooksCollectionPage getRecentNotebooks = graphClient.me().onenote().notebooks()
    .getRecentNotebooks(true)
    .buildRequest()
    .get();

```