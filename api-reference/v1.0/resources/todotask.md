---
title: Тип ресурса Тодотаск
description: Ресурс Тодотаск отслеживает рабочий элемент.
author: avijityadav
localization_priority: Normal
ms.prod: outlook
doc_type: resourcePageType
ms.openlocfilehash: f578df4189d70e6fc9c82d4cd5c038e3cd2de7a2
ms.sourcegitcommit: d9457ac1b8c2e8ac4b9604dd9e116fd547d2bfbb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2020
ms.locfileid: "48797314"
---
# <a name="todotask-resource-type"></a>Тип ресурса Тодотаск

Пространство имен: microsoft.graph

**Тодотаск** представляет задачу, например фрагмент рабочего или личного элемента, которые можно отслеживать и заполнять. 

**Тодотаск** всегда находится в [тодотасклист](todotasklist.md). Он включает связь с коллекцией объектов [линкедресаурце](./linkedResource.md) , отслеживая один или несколько источников задачи.

Этот ресурс поддерживает следующие компоненты:
* Добавление данных в качестве настраиваемых свойств в [открытые расширения](/graph/extensibility-overview).
* Использование [запроса изменений](/graph/delta-query-overview) для отслеживания добавочных дополнений, удалений и обновлений.

## <a name="methods"></a>Методы
|Метод|Тип возвращаемых данных|Описание|
|:---|:---|:---|
|[Перечисление задач](../api/todotasklist-list-tasks.md)|Коллекция [todoTask](todotask.md)|Получение всех ресурсов [todoTask](todotask.md) в указанном списке.|
|[Создание задачи](../api/todotasklist-post-tasks.md)|[todoTask](todotask.md)| Создание объекта [тодотаск](todotask.md) в указанном списке задач|
|[Вывод задачи](../api/todotask-get.md)|[todoTask](../resources/todotask.md)|Чтение свойств и связей объекта [тодотаск](../resources/todotask.md) .|
|[Обновление задачи](../api/todotask-update.md)|[todoTask](../resources/todotask.md)|Обновление свойств объекта [тодотаск](../resources/todotask.md) .|
|[Удаление задачи](../api/todotask-delete.md)|Нет|Удаляет объект [тодотаск](../resources/todotask.md) .|
|[Список Линкедресаурцес](../api/todotask-list-linkedresources.md)|Коллекция [линкедресаурце](../resources/linkedresource.md)|Получение Линкедресаурцес из свойства навигации Линкедресаурцес.|
|[Создание Линкедресаурцес](../api/todotask-post-linkedresources.md)|[линкедресаурце](../resources/linkedresource.md)|Создание нового объекта Линкедресаурцес.|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|body|[itemBody](../resources/itembody.md)|Текст задачи, который обычно содержит сведения о задаче.|
|бодиластмодифиеддатетиме|DateTimeOffset|Дата и время последнего изменения задачи. По умолчанию используется формат UTC. Можно указать пользовательский часовой пояс в заголовке запроса. Значение свойства представлено в формате ISO 8601 (всегда используется формат UTC). Например, полночь UTC 1 января 2020: ' 2020 – 01 – 01T00:00:00Z '.|
|completedDateTime|[dateTimeTimeZone](../resources/datetimetimezone.md)|Дата в указанном часовом поясе, когда задача была завершена.|
|createdDateTime|DateTimeOffset|Дата и время создания задачи. По умолчанию используется формат UTC. Можно указать пользовательский часовой пояс в заголовке запроса. Значение свойства представлено в формате ISO 8601. Например, полночь UTC 1 января 2020: ' 2020 – 01 – 01T00:00:00Z '.|
|dueDateTime|[dateTimeTimeZone](../resources/datetimetimezone.md)|Дата в указанном часовом поясе, когда задача должна быть завершена.|
|id|String|Уникальный идентификатор задачи. По умолчанию это значение изменяется при перемещении элемента из одного списка в другой.|
|importance|importance|Важность задачи. Возможные значения: `low`, `normal`, `high`.|
|isReminderOn|Boolean|Присвоено значение true, если установлено напоминание пользователю о задаче.|
|lastModifiedDateTime|DateTimeOffset|Дата и время последнего изменения задачи. По умолчанию используется формат UTC. Можно указать пользовательский часовой пояс в заголовке запроса. Значение свойства представлено в формате ISO 8601 (всегда используется формат UTC). Например, полночь UTC 1 января 2020: ' 2020 – 01 – 01T00:00:00Z '.|
|recurrence|[patternedRecurrence](../resources/patternedrecurrence.md)|Расписание повторения задачи.|
|reminderDateTime|[dateTimeTimeZone](../resources/datetimetimezone.md)|Дата и время появления напоминания о задаче.|
|status|таскстатус|Указывает состояние или ход выполнения задачи. Возможные значения: `notStarted`, `inProgress`, `completed`, `waitingOnOthers`, `deferred`.|
|title|String|Краткое описание задачи.|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|extensions|Коллекция объектов [extension](extension.md)| Коллекция открытых расширений, определенных для задачи. Допускается значение null.|
|линкедресаурцес|Коллекция [линкедресаурце](../resources/linkedresource.md)|Коллекция ресурсов, связанных с задачей.|


## <a name="json-representation"></a>Представление JSON
Ниже указано представление ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.todoTask",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.todoTask",
  "id": "String (identifier)",
  "body": {
    "@odata.type": "microsoft.graph.itemBody"
  },
  "completedDateTime": {
    "@odata.type": "microsoft.graph.dateTimeTimeZone"
  },
  "dueDateTime": {
    "@odata.type": "microsoft.graph.dateTimeTimeZone"
  },
  "importance": "String",
  "isReminderOn": "Boolean",
  "recurrence": {
    "@odata.type": "microsoft.graph.patternedRecurrence"
  },
  "reminderDateTime": {
    "@odata.type": "microsoft.graph.dateTimeTimeZone"
  },
  "status": "String",
  "title": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "bodyLastModifiedDateTime": "String (timestamp)"
}
```



