---
title: Тип ресурса Ипнамедлокатион
description: Представляет Azure Active Directory с именем Location, заданным диапазонами IP-адресов. Именованные расположения — это настраиваемые правила, определяющие сетевые расположения, которые можно использовать в политике условного доступа.
localization_priority: Normal
author: videor
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: b3863f4902ea0353e7d742b913f89e6d97446ded
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47967473"
---
# <a name="ipnamedlocation-resource-type"></a>Тип ресурса Ипнамедлокатион

Пространство имен: microsoft.graph

Представляет Azure Active Directory с именем Location, заданным диапазонами IP-адресов. Именованные расположения — это настраиваемые правила, определяющие сетевые расположения, которые можно использовать в политике условного доступа.

Наследуется от [намедлокатион](../resources/namedLocation.md)

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип | Описание |
|:-------------|:------------|:------------|
| [Список Ипнамедлокатионс](../api/conditionalaccessroot-list-namedlocations.md) | Коллекция [ипнамедлокатион](ipNamedLocation.md) | Получение всех объектов **ипнамедлокатион** в Организации. |
| [Создание Ипнамедлокатион](../api/conditionalaccessroot-post-namedlocations.md) | [ипнамедлокатион](ipNamedLocation.md) | Создание нового объекта **ипнамедлокатион** . |
| [Получение Ипнамедлокатион](../api/ipnamedlocation-get.md) | [ипнамедлокатион](ipnamedlocation.md) | Чтение свойств и связей объекта **ипнамедлокатион** . |
| [Обновление Ипнамедлокатион](../api/ipnamedlocation-update.md) | [ипнамедлокатион](ipnamedlocation.md) | Обновление объекта **ипнамедлокатион** . |
| [Удаление Ипнамедлокатион](../api/ipnamedlocation-delete.md) | Нет | Удаление объекта **ипнамедлокатион** . |

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|createdDateTime|DateTimeOffset|Тип timestamp представляет дату и время создания расположения с использованием формата ISO 8601 и всегда задается в формате UTC. Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`. Только для чтения. Наследуется от [намедлокатион](../resources/namedLocation.md).|
|displayName|String|Удобное для человека имя расположения.|
|id|String|Идентификатор объекта Намедлокатион. Только для чтения. Наследуется от [намедлокатион](../resources/namedLocation.md).|
|ипранжес|Коллекция объектов [ipRange](iprange.md)|Список диапазонов IP-адресов в формате CIDR IPv4 (например, 1.2.3.4/32) или любом допустимом формате IPv6 из IETF RFC596.|
|Доверять|Boolean|Значение true, если данное расположение явно является доверенным.|
|modifiedDateTime|DateTimeOffset|Тип timestamp представляет дату и время последнего изменения расположения с использованием формата ISO 8601, которое всегда задается в формате UTC. Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`. Только для чтения. Наследуется от [намедлокатион](../resources/namedLocation.md).|

## <a name="relationships"></a>Связи

Отсутствуют.

## <a name="json-representation"></a>Представление в формате JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.ipNamedLocation",
  "baseType": ""
}-->

```json
{
  "createdDateTime": "String (timestamp)",
  "displayName": "String",
  "id": "String (identifier)",
  "ipRanges": [{"@odata.type": "microsoft.graph.ipRange"}],
  "isTrusted": true,
  "modifiedDateTime": "String (timestamp)"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ipNamedLocation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

