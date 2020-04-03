---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: fe524feab77142096f8a8d97c929a97e06d4b578
ms.sourcegitcommit: 33ffed5b785abf36b1a7786856c9266958830d25
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2020
ms.locfileid: "42947105"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

GroupSetting groupSetting = new GroupSetting();
groupSetting.displayName = "GroupSettings";
groupSetting.templateId = "08d542b9-071f-4e16-94b0-74abb372e3d9";
LinkedList<SettingValue> valuesList = new LinkedList<SettingValue>();
SettingValue values = new SettingValue();
values.name = "AllowToAddGuests";
values.value = "false";
valuesList.add(values);
groupSetting.values = valuesList;

graphClient.groups("{id}").settings("{id}")
    .buildRequest()
    .patch(groupSetting);

```