---
title: Тип ресурса Оптионалклаим
description: Содержит необязательное утверждение, связанное с приложением.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: a62176c1e662b1d292f6f359cb2021fae684f4ee
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "37936050"
---
# <a name="optionalclaim-resource-type"></a>Тип ресурса Оптионалклаим

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Содержит необязательное утверждение, связанное с [приложением](application.md) <!-- or a service principal -->. Свойства **идтокен**, **accessToken**и **saml2Token** ресурса [оптионалклаимс](optionalclaims.md) — это коллекция **оптионалклаим**. Если это поддерживается определенным утверждением, вы также можете изменить поведение Оптионалклаим с помощью `additionalProperties` свойства. 

Дополнительные сведения см. [в статье предоставление дополнительных утверждений для приложения Azure AD](https://docs.microsoft.com/azure/active-directory/develop/active-directory-optional-claims) .

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|аддитионалпропертиес|Коллекция строк| Дополнительные свойства утверждения. Если свойство существует в этой коллекции, оно изменяет поведение необязательного утверждения, указанного в свойстве Name. |
|основы|Логический| Если задано значение true, то требование, заданное клиентом, необходимо, чтобы обеспечить гладкую авторизацию для конкретной задачи, запрашиваемой конечным пользователем. Значение по умолчанию  false.|
|name|String| Имя необязательного утверждения. |
|source|Строка| Источник утверждения (объект каталога). В свойствах расширения существуют предопределенные утверждения и пользовательские утверждения. Если исходное значение равно null, утверждение является предварительно определенным необязательным утверждением. Если исходное значение — User, то значение свойства Name — это свойство Extension объекта User. |

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