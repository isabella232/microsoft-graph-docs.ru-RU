---
title: Тип ресурса Директоридефинитион
description: Предоставляет сведения о модуле синхронизации для каталога и его объектов.
localization_priority: Normal
doc_type: resourcePageType
author: ArvindHarinder1
ms.prod: microsoft-identity-platform
ms.openlocfilehash: ccafa9d6763339c32102ace1572c85148f793fc6
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48089296"
---
# <a name="directorydefinition-resource-type"></a>Тип ресурса Директоридефинитион

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Предоставляет сведения о модуле синхронизации для каталога и его объектов. Этот ресурс сообщает обработчику синхронизации, например, что каталог содержит объекты с именем **User** и **Group**, какие атрибуты поддерживаются для этих объектов, и типы этих атрибутов. Чтобы объект и атрибут участвовали в [правилах синхронизации](synchronization-synchronizationrule.md) и [сопоставлениях объектов](synchronization-objectmapping.md), они должны быть определены как часть определения каталога.

Как правило, [схема синхронизации](synchronization-synchronizationschema.md) по умолчанию, предоставляемая как часть [шаблона синхронизации](synchronization-synchronizationtemplate.md) , определяет наиболее часто используемые объекты и атрибуты для этого каталога. Тем не менее, если каталог поддерживает добавление настраиваемых атрибутов, можно расширить определение DEFAULT с использованием собственных настраиваемых объектов или атрибутов. Дополнительные сведения см. в статье [Настройка синхронизации с настраиваемыми атрибутами](synchronization-configure-with-custom-target-attributes.md) и [Настройка синхронизации с атрибутами расширения каталога](synchronization-configure-with-directory-extension-attributes.md).

Определения каталогов обновляются в составе [схемы синхронизации](synchronization-synchronizationschema.md).

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип  |Описание|
|:---------------|:--------|:----------|
|[Обнаружение Директоридефинитион](../api/directorydefinition-discover.md) | [директоридефинитион](synchronization-directorydefinition.md) |Определение схемы и поддерживаемых свойств каталога.|

## <a name="properties"></a>Свойства

| Свойство      | Тип      | Описание    |
|:--------------|:----------|:---------------|
|id           |Строка     |Идентификатор каталога. Значение null не допускается.|
|метаданных       |Коллекция Метадатаентри    |Дополнительные свойства расширения. Если явно не указано иное, значения метаданных не должны изменяться.|
|name           |String     |Имя каталога. Должно быть уникальным в пределах [схемы синхронизации](synchronization-synchronizationschema.md). Значение null не допускается.|
|см        |Коллекция [обжектдефинитион](synchronization-objectdefinition.md)    |Коллекция объектов, поддерживаемая каталогом.|
|version|String|Значение только для чтения, которое указывает обнаруженную версию. Значение null, если обнаружение еще не выполнялось.|
|дисковеридатетиме|DateTimeOffset| Представляет дату и время обнаружения с использованием формата ISO 8601 и всегда задается в формате UTC. Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.|
|дисковерабилитиес|string| Значение только для чтения, указывающее тип обнаружения, поддерживаемый приложением. Возможные значения: `AttributeDataTypes`, `AttributeNames`, `AttributeReadOnly`, `None`, `ReferenceAttributes`, `UnknownFutureValue`.| 

## <a name="json-representation"></a>Представление в формате JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directoryDefinition"
}-->

```json
{
  "discoverabilities": "String",
  "discoveryDateTime": "DateTimeOffset",
  "id": "String",
  "metadata": [{"@odata.type": "microsoft.graph.stringKeyStringValuePair"}],
  "name": "String",
  "objects": [{"@odata.type": "microsoft.graph.objectDefinition"}],
  "version": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "directoryDefinition resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


