---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 54875cc667a755cfaf48f83b3ff026d8a46c758d
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40866359"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Call call = new Call();
call.callbackUri = "https://bot.contoso.com/callback";
LinkedList<InvitationParticipantInfo> targetsList = new LinkedList<InvitationParticipantInfo>();
InvitationParticipantInfo targets = new InvitationParticipantInfo();
IdentitySet identity = new IdentitySet();
Identity user = new Identity();
user.displayName = "John";
user.id = "112f7296-5fa4-42ca-bae8-6a692b15d4b8";
identity.user = user;
targets.identity = identity;
targetsList.add(targets);
call.targets = targetsList;
LinkedList<String> requestedModalitiesList = new LinkedList<String>();
requestedModalitiesList.add("audio");
call.requestedModalities = requestedModalitiesList;
ServiceHostedMediaConfig mediaConfig = new ServiceHostedMediaConfig();
call.mediaConfig = mediaConfig;

graphClient.communications().calls()
    .buildRequest()
    .post(call);

```