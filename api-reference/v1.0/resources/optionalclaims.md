---
title: Тип Оптионалклаимс
description: Объявляет необязательные утверждения, запрошенные приложением.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: sureshja
ms.openlocfilehash: f07b58bd8e5cff9f491f6e20eb11c8afb8654847
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47967361"
---
# <a name="optionalclaims-resource-type"></a>Тип ресурса Оптионалклаимс

Пространство имен: Microsoft. Graph объявляет необязательные утверждения, запрошенные приложением. Приложение может настраивать дополнительные утверждения, возвращаемые в каждом из трех типов маркеров (маркер идентификатора, маркер доступа, маркер SAML 2), которые могут быть получены из службы маркеров безопасности. Приложение может настроить другой набор необязательных утверждений, которые будут возвращаться в каждом типе токена. Свойство Оптионалклаимс [приложения](application.md) является объектом **оптионалклаимс** .

Разработчики приложений могут настраивать необязательные утверждения в своих приложениях Azure AD, чтобы указать, какие утверждения им нужны в маркерах, отправляемых в приложения службой маркеров безопасности (Майкрософт). Дополнительные сведения см. в статье [Предоставление необязательных утверждений для приложения Azure AD](/azure/active-directory/develop/active-directory-optional-claims).

## <a name="properties"></a>Свойства
| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|идтокен|Коллекция [оптионалклаим](optionalclaim.md)| Необязательные утверждения, возвращенные в маркере идентификатора JWT. |
|accessToken|Коллекция [оптионалклаим](optionalclaim.md)| Необязательные утверждения, возвращенные в маркере доступа JWT. |
|saml2Token|Коллекция [оптионалклаим](optionalclaim.md)| Необязательные утверждения, возвращенные в маркере SAML.|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.optionalClaims"
}-->
``` json
{
  "idToken": [{"@odata.type": "microsoft.graph.optionalClaim"}],
  "accessToken": [{"@odata.type": "microsoft.graph.optionalClaim"}],
  "saml2Token": [{"@odata.type": "microsoft.graph.optionalClaim"}]
}
```
