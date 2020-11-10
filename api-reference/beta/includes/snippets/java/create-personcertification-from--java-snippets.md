---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 709f6872cacd6bb25ca9985c929b7b8d4e8defb5
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48967273"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

PersonCertification personCertification = new PersonCertification();
personCertification.certificationId = "KB-1235466333663322";
personCertification.description = "Blackbelt in Marketing - Brand Management";
personCertification.displayName = "Marketing Blackbelt - Brand Management";
personCertification.thumbnailUrl = "https://iame.io/dfhdfdfd334.jpg";
personCertification.webUrl = "https://www.iame.io/blackbelt";

graphClient.me().profile().certifications()
    .buildRequest()
    .post(personCertification);

```