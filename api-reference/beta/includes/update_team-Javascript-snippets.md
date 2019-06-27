---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: fe6b28e778100cfbfb6c5d114cea02e9dfe141e9
ms.sourcegitcommit: 0e1101d499f35b08aa2309e273871438b1774979
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2019
ms.locfileid: "35263744"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const team = {
  memberSettings: {
    allowCreateUpdateChannels: true
  },
  messagingSettings: {
    allowUserEditMessages: true,
    allowUserDeleteMessages: true
  },
  funSettings: {
    allowGiphy: true,
    giphyContentRating: "strict"
  },
  discoverySettings: {
    showInTeamsSearchAndSuggestions: true
  }
};

let res = await client.api('/teams/{id}')
    .version('beta')
    .update({team : team});

```