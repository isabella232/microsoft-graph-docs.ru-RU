---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a9fc5751d93eb703deec762a5e61c720d0b9797f
ms.sourcegitcommit: c20276369a8834a259f24038e7ee5c33de02660b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/07/2020
ms.locfileid: "48373461"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Channel channel = new Channel();
channel.displayName = "Architecture Discussion";
channel.description = "This channel is where we debate all future architecture plans";
channel.membershipType = ChannelMembershipType.STANDARD;

graphClient.teams("{id}").channels()
    .buildRequest()
    .post(channel);

```