---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 47d56be493034680eaece13b3c5d44fce701bad3
ms.sourcegitcommit: c9b9ff2c862f8d96d282a7bdf641cdb9c53a4600
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2019
ms.locfileid: "37636987"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const event = {
  subject: "Plan summer company picnic",
  body: {
    contentType: "HTML",
    content: "Let's kick-start this event planning!"
  },
  start: {
      dateTime: "2017-08-30T11:00:00",
      timeZone: "Pacific Standard Time"
  },
  end: {
      dateTime: "2017-08-30T12:00:00",
      timeZone: "Pacific Standard Time"
  },
  attendees: [
    {
      emailAddress: {
        address: "DanaS@contoso.onmicrosoft.com",
        name: "Dana Swope"
      },
      type: "Required"
    },
    {
      emailAddress: {
        address: "AlexW@contoso.onmicrosoft.com",
        name: "Alex Wilber"
      },
      type: "Required"
    }
  ],
  location: {
    displayName: "Conf Room 3; Fourth Coffee; Home Office",
    locationType: "Default"
  },
  locations: [
    {
      displayName: "Conf Room 3"
    },
    {
      displayName: "Fourth Coffee",
      address: {
        street: "4567 Main St",
        city: "Redmond",
        state: "WA",
        countryOrRegion: "US",
        postalCode: "32008"
      },
      coordinates: {
        latitude: 47.672,
        longitude: -102.103
      }
    },
    {
      displayName: "Home Office"
    }
  ],
  allowNewTimeProposals: true
};

let res = await client.api('/me/events')
    .version('beta')
    .post(event);

```