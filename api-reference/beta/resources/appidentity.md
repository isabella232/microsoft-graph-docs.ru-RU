---
title: Тип ресурса Аппидентити
description: Указывает идентификатор приложения, который выполнил действие или изменился. Включает идентификатор приложения, имя, идентификатор и имя участника службы. Этот ресурс вызывается API Директоряудит
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: sureshja
ms.openlocfilehash: ed814cb4e096ff8e13bdb8f06ede6cad4f94c6d5
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48004202"
---
# <a name="appidentity-resource-type"></a>Тип ресурса Аппидентити

Пространство имен: Microsoft. Graph указывает идентификатор приложения, который выполнил действие или изменился. Включает идентификатор приложения, имя, идентификатор и имя участника службы. Этот ресурс вызывается API [директоряудит](../api/directoryaudit-get.md)


## <a name="properties"></a>Свойства
| Свойство     | Тип   |Описание|
|:---------------|:--------|:----------|
|appId|String|Обозначает уникальный идентификатор GUID, представляющий идентификатор приложения в Azure Active Directory.|
|displayName|String|Указывает на имя приложения, отображаемое на портале Azure.|
|сервицепринЦипалид|String|Указывает уникальный идентификатор GUID, указывающий идентификатор участника службы в Azure Active Directory для соответствующего приложения.|
|servicePrincipalName|String|— Имя участника-службы — это имя приложения в клиенте. |

## <a name="json-representation"></a>Представление в формате JSON

Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.appIdentity"
}-->

```json
{
  "appId": "String",
  "displayName": "String",
  "servicePrincipalId": "String",
  "servicePrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "appIdentity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


