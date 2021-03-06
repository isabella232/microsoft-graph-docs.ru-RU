---
title: Тип ресурса Акцесспаккажекаталог
description: Каталог пакетов Access — это контейнер для пакетов Access.
localization_priority: Normal
author: markwahl-msft
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 3d8c93defc8d76fbee1efbc162677f21b4e7f827
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48089856"
---
# <a name="accesspackagecatalog-resource-type"></a>Тип ресурса Акцесспаккажекаталог

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

В [управлении обслуживанием Azure AD](entitlementmanagement-root.md)каталог пакетов Access — это контейнер для одного или нескольких пакетов доступа.  Каталог пакетов Access также может иметь связанные ресурсы, которые используются в этих пакетах доступа для предоставления доступа.


## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип | Описание |
|:-------------|:------------|:------------|
| [Список Акцесспаккажекаталогс](../api/accesspackagecatalog-list.md) | Коллекция [акцесспаккажекаталог](accesspackagecatalog.md) | Получение списка объектов акцесспаккажекаталог. |
| [Создание Акцесспаккажекаталог](../api/accesspackagecatalog-post.md) | [акцесспаккажекаталог](accesspackagecatalog.md) | Создание нового объекта Акцесспаккажекаталог. |
| [Получение Акцесспаккажекаталог](../api/accesspackagecatalog-get.md) | [акцесспаккажекаталог](accesspackagecatalog.md) | Чтение свойств и связей объекта Акцесспаккажекаталог. |
| [Обновление Акцесспаккажекаталог](../api/accesspackagecatalog-update.md)|Нет | Обновление свойств объекта Акцесспаккажекаталог. |
| [Удаление Акцесспаккажекаталог](../api/accesspackagecatalog-delete.md) | | Удаление Акцесспаккажекаталог. |
| [Список ресурсов Акцесспаккажекаталог](../api/accesspackagecatalog-list-accesspackageresources.md) | Коллекция [акцесспаккажересаурце](accesspackageresource.md) | Получение списка объектов Акцесспаккажересаурце в каталоге. |
| [Список ролей ресурсов Акцесспаккажекаталог](../api/accesspackagecatalog-list-accesspackageresourceroles.md) | Коллекция [акцесспаккажересаурцероле](accesspackageresourcerole.md) | Получение списка объектов Акцесспаккажересаурцероле для ресурсов в каталоге. |

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|каталогстатус|Строка|Имеет значение, `Published` Если пакеты доступа доступны для управления.|
|каталогтипе|Строка|Один из `UserManaged` или `ServiceDefault` . |
|createdBy|Строка|Имя участника-пользователя, создавшего этот ресурс. Только для чтения.|
|createdDateTime|DateTimeOffset|Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`. Только для чтения.|
|description|Строка|Описание каталога пакетов Access.|
|displayName|Строка|Отображаемое имя каталога пакетов Access.|
|id|String| Только для чтения.|
|исекстерналливисибле|Boolean|Указывает, могут ли пользователи за пресети клиента запрашивать пакеты доступа в этом каталоге.|
|модифиедби|Строка|Имя участника-пользователя, который последним изменил этот ресурс. Только для чтения.|
|modifiedDateTime|DateTimeOffset|Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`. Только для чтения. |


## <a name="relationships"></a>Связи

| Связь | Тип        | Описание |
|:-------------|:------------|:------------|
|акцесспаккажес|Коллекция [акцесспаккаже](accesspackage.md)| Пакеты Access в этом каталоге. Только для чтения. Допускается значение null.|
|акцесспаккажересаурцес|Коллекция [акцесспаккажересаурце](accesspackageresource.md)| Только для чтения. Допускается значение null.|

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.accessPackageCatalog",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
    "id":"360fa7de-90be-48dc-a2ce-fc40094a93dd",
    "description":"Sample access package catalog",
    "displayName":"Access package catalog for testing",
    "isExternallyVisible":false,
    "catalogType":"UserManaged",
    "catalogStatus":"Published",
    "createdDateTime":"2019-01-27T18:19:50.74Z",
    "modifiedDateTime":"2019-01-27T18:19:50.74Z",
    "createdBy":"TestGA@example.com",
    "modifiedBy":"TestGA@example.com"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "accessPackageCatalog resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


