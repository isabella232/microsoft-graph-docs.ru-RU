---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: de90a74b56be163689a7e492c3b8a7a6f26d935e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35528690"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const accessReviewReviewer = {
    id:"006111db-0810-4494-a6df-904d368bd81b"
};

let res = await client.api('/accessReviews/2b83cc42-09db-46f6-8c6e-16fec466a82d/reviewers')
    .version('beta')
    .post({accessReviewReviewer : accessReviewReviewer});

```