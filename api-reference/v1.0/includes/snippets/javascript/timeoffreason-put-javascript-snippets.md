---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: c49a040e44baebf3a911421f5916d9a041efdd70
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2020
ms.locfileid: "44218300"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const timeOffReason = {
  displayName: "Vacation",
  iconType: "plane",
  isActive: true
};

let res = await client.api('/teams/{teamId}/schedule/timeOffReasons/{timeOffReasonId}')
    .put(timeOffReason);

```