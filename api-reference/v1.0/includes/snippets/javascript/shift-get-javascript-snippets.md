---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d471d145e043c9728f30040a9ba131102613cf80
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "44684172"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const shiftPreferences = {
    id: "SHPR_eeab4fb1-20e5-48ca-ad9b-98119d94bee7",
    @odata.etag: "1a371e53-f0a6-4327-a1ee-e3c56e4b38aa",
    availability: [
        {
            recurrence: {
                pattern: {
                    type: "Weekly",
                    daysOfWeek: ["Monday", "Wednesday", "Friday"],
                    interval: 1
                },
                range: {
                    type: "noEnd"
                }
            },
            timeZone: "Pacific Standard Time",
            timeSlots: null
        }
    ]
};

let res = await client.api('/users/871dbd5c-3a6a-4392-bfe1-042452793a50/settings/shiftPreferences')
    .update(shiftPreferences);

```