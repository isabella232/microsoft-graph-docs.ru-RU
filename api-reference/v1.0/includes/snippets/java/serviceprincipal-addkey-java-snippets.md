---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 9340ae109720d28ba6892a2fa5715b1827393a7c
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48983226"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

KeyCredential keyCredential = new KeyCredential();
keyCredential.type = "X509CertAndPassword";
keyCredential.usage = "Sign";
keyCredential.key = Base64.getDecoder().decode("MIIDYDCCAki...");

PasswordCredential passwordCredential = new PasswordCredential();
passwordCredential.secretText = "MKTr0w1...";

String proof = "eyJ0eXAiOiJ...";

graphClient.servicePrincipals("{id}")
    .addKey(keyCredential,passwordCredential,proof)
    .buildRequest()
    .post();

```