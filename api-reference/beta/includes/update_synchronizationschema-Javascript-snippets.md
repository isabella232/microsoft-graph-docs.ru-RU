---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 34f3cc862a7c348c9297171258c85a174905cf20
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2019
ms.locfileid: "34475985"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const synchronizationSchema = {
    directories: [
        {
            name: "Azure Active Directory",
            objects: [
                {
                    name: "User",
                    attributes: [
                        {
                            name: "userPrincipalName",
                            type: "string"
                        }
                    ]
                },
            ]
        },
        {
            name: "Salesforce",
        }
    ],
    synchronizationRules:[
        {
            name: "USER_TO_USER",
            sourceDirectoryName: "Azure Active Directory",
            targetDirectoryName: "Salesforce",
            objectMappings: [
                {
                    sourceObjectName: "User",
                    targetObjectName: "User",
                    attributeMappings: [
                        {
                            source: {},
                            targetAttributeName: "userName"
                        },
                    ]
                },
            ]
        },
    ]
};

let res = await client.api('/servicePrincipals/{id}/synchronization/jobs/{jobId}/schema')
    .version('beta')
    .put({synchronizationSchema : synchronizationSchema});

```