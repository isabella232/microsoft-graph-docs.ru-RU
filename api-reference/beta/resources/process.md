---
title: Тип ресурса "процесс"
description: " > **Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены. Использование этих API в производственных приложениях не поддерживается."
localization_priority: Normal
doc_type: resourcePageType
ms.prod: ''
author: preetikr
ms.openlocfilehash: a024cfbabcff4357427ae6a814da00af83eae304
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48070494"
---
# <a name="process-resource-type"></a>Тип ресурса "процесс"

Пространство имен: microsoft.graph

 [!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Содержит сведения о состоянии процесса, связанного с оповещением.

## <a name="properties"></a>Свойства

| Свойство   | Тип|Описание|
|:---------------|:--------|:----------|
|accountName|String|Идентификатор учетной записи пользователя (контекст учетной записи пользователя, который выполнялся в данный процесс) например, имя_учетной_записи, SID и т. д.|
|commandLine|String|Командная строка вызова полной обработки, включая все параметры.|
|createdDateTime|DateTimeOffset|Время запуска процесса. Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.|
|fileHash|[fileHash](filehash.md)|Сложный тип, содержащий хэши файлов (криптография и с учетом расположения).|
|интегритилевел|processIntegrityLevel|Уровень целостности процесса. Возможные значения: `unknown`, `untrusted`, `low`, `medium`, `high`, `system`.|
|Повышенный уровень|Boolean|Значение true, если процесс повышен.|
|name|String|Имя файла образа процесса.|
|парентпроцесскреатеддатетиме|DateTimeOffset|Дата и время начала родительского процесса. Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.|
|парентпроцессид|Int32|Идентификатор процесса (PID) родительского процесса.|
|парентпроцесснаме|String|Имя файла образа родительского процесса.|
|path|String|Полный путь, включая имя файла.|
|processId|Int32|Идентификатор процесса (PID).|

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.process"
}-->

```json
{
  "accountName": "String",
  "commandLine": "String",
  "createdDateTime": "String (timestamp)",
  "fileHash": {"@odata.type": "microsoft.graph.fileHash"},
  "integrityLevel": "@odata.type: microsoft.graph.processIntegrityLevel",
  "isElevated": true,
  "name": "String",
  "parentProcessCreatedDateTime": "String (timestamp)",
  "parentProcessId": 1024,
  "parentProcessName": "String",
  "path": "String",
  "processId": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "process resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


