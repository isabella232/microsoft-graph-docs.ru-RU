---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 53819cfe5c05cf353b0c0efa122808f3b10740a6
ms.sourcegitcommit: d4114bac58628527611e83e436132c6581a19c52
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2020
ms.locfileid: "44217288"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/teamwork/workforceIntegrations/{workforceIntegrationId}')
    .delete();

```