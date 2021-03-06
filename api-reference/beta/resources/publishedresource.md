---
title: Тип ресурса Публишедресаурце
description: Тип ресурса Публишедресаурце.
localization_priority: Normal
author: japere
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 4a5f75b6bd12299275e8002abc5c3991984d06e8
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48026413"
---
# <a name="publishedresource-resource-type"></a>Тип ресурса Публишедресаурце

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет локальный опубликованный ресурс. Администратор клиента может публиковать различные типы локальных ресурсов, корпоративных приложений, контроллеров домена, серверов и т. д. [локальные агенты](onpremisesagent.md) , установленные администратором клиента, можно настроить для доступа к определенному опубликованному ресурсу или обработки запросов.

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип | Описание |
|:-------------|:------------|:------------|
| [Список Публишедресаурцес](../api/publishedresource-list.md) | Коллекция объектов [публишедресаурце](publishedresource.md) | Получение коллекции объектов **публишедресаурцес** . |
| [Получение Публишедресаурце](../api/publishedresource-get.md) | [публишедресаурце](publishedresource.md) | Чтение свойств и связей объекта **публишедресаурце** . |
| [Создание Публишедресаурце](../api/publishedresource-post.md) |  [публишедресаурце](publishedresource.md)  | Создание нового **публишедресаурце**. |
| [Обновление Публишедресаурце](../api/publishedresource-update.md) | [публишедресаурце](publishedresource.md) | Обновление объекта **публишедресаурце** . |
| [Удаление Публишедресаурце](../api/publishedresource-delete.md) | Нет | Удаление объекта **публишедресаурце** . |
| [Назначение Публишедресаурце для Онпремисесажентграуп](../api/publishedresource-post-agentgroups.md) | Нет | Назначьте объект **публишедресаурце** для **онпремисесажентграуп**. |
| [Удаление Публишедресаурце из Онпремисесажентграуп](../api/publishedresource-delete-agentgroups.md) | Нет |  Удаление объекта **публишедресаурце** из объекта **онпремисесажентграуп**.|

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|displayName|String| Отображаемое имя Публишедресаурце.|
|id|String| Идентификатор объекта Публишедресаурце. Только для чтения.|
|публишингтипе|string| Возможные значения: `applicationProxy`, `exchangeOnline`, `authentication`, `provisioning`, `adAdministration`.|
|resourceName|String|Имя Публишедресаурце.|

## <a name="relationships"></a>Отношения

| Связь | Тип        | Описание |
|:-------------|:------------|:------------|
|ажентграупс|Коллекция [онпремисесажентграуп](onpremisesagentgroup.md)| Список **онпремисесажентграупс** , которым назначено **публишедресаурце** . Только для чтения. Допускается значение null.|

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.publishedResource",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)",
  "publishingType": "string",
  "resourceName": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "publishedResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


