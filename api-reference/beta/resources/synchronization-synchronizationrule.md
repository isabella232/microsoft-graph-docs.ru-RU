---
title: Тип ресурса Синчронизатионруле
description: Определяет способ выполнения синхронизации для обработчика синхронизации.
localization_priority: Normal
doc_type: resourcePageType
author: ArvindHarinder1
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 86a5f39612b6fdbeb123a74372520115e0357fb0
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48023819"
---
# <a name="synchronizationrule-resource-type"></a>Тип ресурса Синчронизатионруле

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Определяет способ выполнения синхронизации для обработчика синхронизации, в том числе объекты, которые необходимо синхронизировать и в каком направлении, как объекты из исходного каталога должны сопоставляться с объектами в целевом каталоге и как должны быть преобразованы атрибуты при их синхронизации из источника в целевой каталог.

>**Примечание:** Правила синхронизации определяют синхронизацию в одном направлении — из исходного каталога в конечный каталог. Исходные и целевые каталоги определяются как часть свойств правила.

Правила синхронизации обновляются в рамках [схемы синхронизации](synchronization-synchronizationschema.md).

## <a name="properties"></a>Свойства

| Свойство      | Тип      | Описание    |
|:--------------|:----------|:---------------|
|редактируем       |Boolean    |`true` значение, если правило синхронизации может быть изменено; `false` если это правило доступно только для чтения и не должно изменяться.|
|id             |String     |Идентификатор правила синхронизации. Допустимые значения: один из идентификаторов, распознаваемый обработчиком синхронизации. Поддерживаемые идентификаторы правил можно найти в шаблоне синхронизации, возвращенном API.|
|метаданных       |Коллекция [стрингкэйстрингвалуепаир](synchronization-stringkeystringvaluepair.md) |Дополнительные свойства расширения. Если вы не укажете в явной форме команду поддержки, значения метаданных не должны изменяться.|
|name           |String     |Понятное имя правила синхронизации. Значение null не допускается.|
|обжектмаппингс |Коллекция [обжектмаппинг](synchronization-objectmapping.md)    |Коллекция сопоставлений объектов, поддерживаемых правилом. Сообщает обработчику синхронизации, какие объекты должны синхронизироваться.|
|priority       |Целое число    |Приоритет относительно других правил в [синчронизатионсчема](synchronization-synchronizationschema.md). Правила с наименьшим номером приоритета будут обработаны первыми.|
|саурцедиректоринаме       |String    |Имя исходного каталога. Должно сопоставляться с одним из определений каталога в [синчронизатионсчема](synchronization-synchronizationschema.md).|
|таржетдиректоринаме       |String    |Имя целевого каталога. Должно сопоставляться с одним из определений каталога в [синчронизатионсчема](synchronization-synchronizationschema.md).|

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationRule"
}-->

```json
{
  "editable": true,
  "id": "String",
  "metadata": [{"@odata.type": "microsoft.graph.stringKeyStringValuePair"}],
  "name": "String",
  "objectMappings": [{"@odata.type": "microsoft.graph.objectMapping"}],
  "priority": 1024,
  "sourceDirectoryName": "String",
  "targetDirectoryName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "synchronizationRule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


