---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 556ab7299743e5a2cac63d1472215ea7bcc68e0d
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40871922"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const threatAssessmentRequest = {
  @odata.type: "#microsoft.graph.fileAssessmentRequest",
  expectedAssessment: "block",
  category: "malware",
  fileName: "test.txt",
  contentData: "VGhpcyBpcyBhIHRlc3QgZmlsZQ=="
};

let res = await client.api('/informationProtection/threatAssessmentRequests')
    .version('beta')
    .post(threatAssessmentRequest);

```