---
title: Тип ресурса Воркбукворкшит
description: Лист Excel представляет собой сетку ячеек. Он может содержать данные, таблицы, диаграммы и т. д.
localization_priority: Normal
author: lumine2008
ms.prod: excel
doc_type: resourcePageType
ms.openlocfilehash: 32cd971eff1583fd5eea58f1ffa34ba720c96bce
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48019427"
---
# <a name="workbookworksheet-resource-type"></a>Тип ресурса Воркбукворкшит

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Лист Excel представляет собой сетку ячеек. Он может содержать данные, таблицы, диаграммы и т. д.


## <a name="methods"></a>Методы

| Метод           | Возвращаемый тип    |Описание|
|:---------------|:--------|:----------|
|[Получение объекта Worksheet](../api/worksheet-get.md) | [воркбукворкшит](workbookworksheet.md) |Чтение свойств и связей объекта листа.|
|[Создание объекта Chart](../api/worksheet-post-charts.md) |[воркбукчарт](workbookchart.md)| Создание диаграммы путем добавления в коллекцию диаграмм.|
|[Список имен](../api/worksheet-list-names.md) |Коллекция [workbookNamedItem](workbooknameditem.md)| Получение коллекции именованных элементов, связанной с листом.|
|[Список диаграмм](../api/worksheet-list-charts.md) |Коллекция [воркбукчарт](workbookchart.md)| Получение коллекции объектов Chart.|
|[Создание объекта Table](../api/worksheet-post-tables.md) |[воркбуктабле](workbooktable.md)| Создание таблицы путем добавления в коллекцию таблиц.|
|[Список таблиц](../api/worksheet-list-tables.md) |Коллекция [workbookTable](workbooktable.md)| Получение коллекции объектов Table.|
|[Update](../api/worksheet-update.md) | [воркбукворкшит](workbookworksheet.md)   |Обновление объекта Worksheet. |
|[Cell](../api/worksheet-cell.md)|[workbookRange](workbookrange.md)|Получает объект диапазона, содержащий одну ячейку, на основе номеров строки и столбца. Ячейка может выходить за пределы родительского диапазона, если она расположена в сетке листа.|
|[Range](../api/worksheet-range.md)|[workbookRange](workbookrange.md)|Возвращает объект диапазона по адресу или имени.|
|[Usedrange](../api/worksheet-usedrange.md)|[workbookRange](workbookrange.md)|Используемый диапазон — это наименьший диапазон, включающий в себя все ячейки, которые содержат значение или форматирование. Если лист пустой, эта функция вернет верхнюю левую ячейку.|
|[Delete](../api/worksheet-delete.md)|Нет|Удаляет лист из книги.|
|[Список](../api/worksheet-list.md) | Коллекция [workbookWorksheet](workbookworksheet.md) |Получение коллекции объектов листов. |
|[Add](../api/worksheetcollection-add.md)|[воркбукворкшит](workbookworksheet.md)|Добавляет новый лист в книгу. Лист будет добавлен после существующих листов. |
|[Список pivotTables](../api/workbookworksheet-list-pivottables.md) |Коллекция [workbookPivotTable](workbookpivottable.md)| Получение коллекции объектов workbookPivotTable.|

## <a name="properties"></a>Свойства
| Свойство     | Тип   |Описание|
|:---------------|:--------|:----------|
|id|string|Возвращает значение, однозначно идентифицирующее лист в данной книге. Значение идентификатора остается прежним, даже если переименовать или переместить лист. Только для чтения.|
|name|string|Отображаемое имя листа.|
|position|int|Положение листа (начиная с нуля) в книге.|
|visibility|string|Видимость листа. Допустимые значения: `Visible`, `Hidden`, `VeryHidden`.|

## <a name="relationships"></a>Отношения
| Связь | Тип   |Описание|
|:---------------|:--------|:----------|
|charts|Коллекция [воркбукчарт](workbookchart.md)|Возвращает коллекцию диаграмм, имеющихся на листе. Только для чтения.|
|names|Коллекция [workbookNamedItem](workbooknameditem.md)|Возвращает коллекцию имен, связанных с листом. Только для чтения.|
|pivotTables|Коллекция [workbookPivotTable](workbookpivottable.md)| Коллекция сводных таблиц на листе. |
|protection|[воркбукворкшитпротектион](workbookworksheetprotection.md)|Возвращает объект защиты листа. Только для чтения.|
|tables|Коллекция [workbookTable](workbooktable.md)|Коллекция таблиц, имеющихся на листе. Только для чтения.|

## <a name="json-representation"></a>Представление JSON

Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookWorksheet"
}-->

```json
{
  "id": "string",
  "name": "string",
  "position": 1024,
  "visibility": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Worksheet resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


