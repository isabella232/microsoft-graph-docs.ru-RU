---
title: Тип ресурса Акцесспаккажересаурце
description: Ресурс пакета Access — это ссылка на ресурс, связанный с каталогом, в котором находятся роли, которые можно использовать в одном или нескольких пакетах доступа.
localization_priority: Normal
author: markwahl-msft
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 6c37ff0de7f733b67eda0541418ca4b42aa57352
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48089835"
---
# <a name="accesspackageresource-resource-type"></a>Тип ресурса Акцесспаккажересаурце

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

В разделе [Управление обслуживанием Azure AD](entitlementmanagement-root.md)ресурс пакета Access — это ссылка на ресурс, связанный с каталогом пакетов Access, роли, которые можно использовать в одном или нескольких пакетах доступа.  Чтобы запросить сопоставление ресурса с каталогом пакетов Access, создайте [акцесспаккажересаурцерекуест](accesspackageresourcerequest.md).

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип | Описание |
|:-------------|:------------|:------------|
| [Список ресурсов Акцесспаккажекаталог](../api/accesspackagecatalog-list-accesspackageresources.md) | Коллекция [акцесспаккажересаурце](accesspackageresource.md) | Получение списка объектов Акцесспаккажересаурце в каталоге. |

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|аддедби|String|Только для чтения.|
|аддедон|DateTimeOffset|Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда используется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.|
|description|Строка|Описание ресурса.|
|displayName|Строка|Отображаемое имя ресурса, например имя приложения, имя группы или имя сайта.|
|id|String| Только для чтения.|
|испендингонбоардинг|Boolean|Значение true, если ресурс пока недоступен для назначения.|
|оригинид|Строка|Уникальный идентификатор ресурса в исходной системе. В случае группы Azure AD это идентификатор группы. |
|оригинсистем|Строка|Тип ресурса в исходной системе, например `SharePointOnline` , `AadApplication` или `AadGroup` .|
|Ресурса|Строка|Тип ресурса, например, `Application` если это приложение, подключаемое к Azure AD, или `SharePoint Online Site` сайт SharePoint Online.|
|url|String|Уникальный указатель ресурсов для ресурса, например URL-адрес для подписания пользователя в приложении.|

## <a name="relationships"></a>Связи

| Связь | Тип        | Описание |
|:-------------|:------------|:------------|
|акцесспаккажересаурцеролес|Коллекция [акцесспаккажересаурцероле](accesspackageresourcerole.md)| Только для чтения. Допускается значение null.|
|акцесспаккажересаурцескопес|Коллекция [акцесспаккажересаурцескопе](accesspackageresourcescope.md)| Только для чтения. Допускается значение null.|

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.accessPackageResource",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "addedBy": "String",
  "addedOn": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "id": "String (identifier)",
  "isPendingOnboarding": true,
  "originId": "String",
  "originSystem": "String",
  "resourceType": "String",
  "url": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "accessPackageResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


