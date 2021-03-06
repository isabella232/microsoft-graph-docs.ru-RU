---
title: Тип ресурса Оптионалклаим
description: УКАЖИТЕ ОПИСАНИЕ
localization_priority: Normal
author: sureshja
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: d5c4391efd7da79c86176b8d45c9bd1d6ba65d56
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48003019"
---
# <a name="optionalclaim-resource-type"></a>Тип ресурса Оптионалклаим

Пространство имен: microsoft.graph

Содержит необязательное утверждение, связанное с [приложением](application.md) <!-- or a service principal -->. `idToken`Свойства, `accessToken` и, в `saml2Token` ресурсе [оптионалклаимс](optionalclaims.md) , представляют собой коллекцию **оптионалклаим**. Если это поддерживается определенным утверждением, вы также можете изменить поведение Оптионалклаим с помощью `additionalProperties` Свойства.

Дополнительные сведения см. в статье [Предоставление необязательных утверждений для приложения Azure AD](/azure/active-directory/develop/active-directory-optional-claims).

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|аддитионалпропертиес|Коллекция String| Дополнительные свойства утверждения. Если свойство существует в этой коллекции, оно изменяет поведение необязательного утверждения, указанного в свойстве Name. |
|основы|Boolean| Если задано значение true, то требование, заданное клиентом, необходимо, чтобы обеспечить гладкую авторизацию для конкретной задачи, запрашиваемой конечным пользователем. Значение по умолчанию  false.|
|name|String| Имя необязательного утверждения. |
|source|String| Источник утверждения (объект каталога). В свойствах расширения существуют предопределенные утверждения и пользовательские утверждения. Если исходное значение равно null, утверждение является предварительно определенным необязательным утверждением. Если исходное значение — User, то значение свойства Name — это свойство Extension объекта User. |

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.optionalClaim",
  "baseType": null
}-->

```json
{
  "additionalProperties": ["String"],
  "essential": true,
  "name": "String",
  "source": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "optionalClaim resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
