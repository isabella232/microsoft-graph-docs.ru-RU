---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: e3243badf01545c5cde8e0abec7f6d16e0d75f80
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48981013"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

MessageRule messageRule = new MessageRule();
messageRule.displayName = "Important from partner";
MessageRuleActions actions = new MessageRuleActions();
actions.markImportance = Importance.HIGH;
messageRule.actions = actions;

graphClient.me().mailFolders("inbox").messageRules("AQAAAJ5dZqA=")
    .buildRequest()
    .patch(messageRule);

```