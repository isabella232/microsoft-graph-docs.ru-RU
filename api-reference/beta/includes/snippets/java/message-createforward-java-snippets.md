---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d4339133233b80fe856b51ec3ef09ae1913d2bae
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48981617"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Message message = new Message();
message.isDeliveryReceiptRequested = true;
LinkedList<Recipient> toRecipientsList = new LinkedList<Recipient>();
Recipient toRecipients = new Recipient();
EmailAddress emailAddress = new EmailAddress();
emailAddress.address = "danas@contoso.onmicrosoft.com";
emailAddress.name = "Dana Swope";
toRecipients.emailAddress = emailAddress;
toRecipientsList.add(toRecipients);
message.toRecipients = toRecipientsList;

String comment = "Dana, just want to make sure you get this; you'll need this if the project gets approved.";

graphClient.me().messages("AAMkADA1MTAAAH5JaLAAA=")
    .createForward(null,message,comment)
    .buildRequest()
    .post();

```