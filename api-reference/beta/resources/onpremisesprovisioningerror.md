---
title: Тип ресурса onPremisesProvisioningError
description: Представляет ошибки синхронизации каталогов для сущностей контактов пользователя, группы или организации при синхронизации локальных каталогов с Azure Active Directory.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: japere
ms.openlocfilehash: ac6ae129374ab33e44a1f3274e8be378b90eb4e1
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48052598"
---
# <a name="onpremisesprovisioningerror-resource-type"></a>Тип ресурса onPremisesProvisioningError

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет ошибки синхронизации каталогов для сущностей контактов [пользователя](user.md), [группы](group.md)или [Организации](orgcontact.md) при синхронизации локальных каталогов с Azure Active Directory.

## <a name="properties"></a>Свойства

| Свойство | Тип | Описание |
|:---------------|:--------|:----------|
|category|String| Категория ошибки подготовки. Примечание. в настоящее время существует только одно возможное значение. Возможное значение: *пропертиконфликт* — указывает, что значение свойства не является уникальным. Другие объекты содержат одно и то же значение свойства. |
|оккурреддатетиме|DateTimeOffset| Дата и время возникновения ошибки. |
|пропертикаусинжеррор|String| Имя свойства каталога, вызвавшего ошибку. Текущие возможные значения: *userPrincipalName* или *proxyAddress* |
|value|String| Значение свойства, вызвавшего ошибку. |

## <a name="json-representation"></a>Представление в формате JSON
Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesProvisioningError"
}-->

```json
{
  "category": "String",
  "occurredDateTime": "String (timestamp)",
  "propertyCausingError": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "onPremisesProvisioningError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


