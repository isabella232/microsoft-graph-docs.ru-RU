---
title: Тип ресурса directoryRole
description: Представляет роль каталога Azure AD. Роли каталога Azure AD также известны как *роли администратора*.
localization_priority: Normal
author: abhijeetsinha
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: bec9df52add7ab5a3c0440f3d7c7896d2920370a
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "48402291"
---
# <a name="directoryrole-resource-type"></a>Тип ресурса directoryRole

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет роль каталога Azure AD. Роли каталога Azure AD также известны как *роли администратора*. Для получения дополнительных сведений о ролях каталога (администратора) см. статью [Назначение ролей администратора в Azure AD](/azure/active-directory/users-groups-roles/directory-assign-admin-roles). С помощью Microsoft Graph можно назначать пользователям роли каталога, чтобы предоставить им разрешения целевой роли. Чтобы можно было считать роль каталога или обновить ее членов, сначала следует активировать ее на клиенте. По умолчанию активируется только роль каталога администраторов организации. Чтобы активировать другие доступные роли каталога, отправьте запрос POST с ИДЕНТИФИКАТОРом [directoryRoleTemplate](directoryroletemplate.md) , на котором основана роль каталога. [Перечислите шаблоны для ролей каталогов](../api/directoryroletemplate-list.md), чтобы получить все остальные доступные роли каталогов. Наследуется от [directoryObject](directoryobject.md).

По умолчанию роли каталога разделяются на уровне клиента.  Однако роли каталогов (в настоящее время только *Администратор учетной записи пользователя* и *администратор службы поддержки*) также могут быть ограничены [административными единицами](administrativeunit.md).

Этот ресурс поддерживает:

- отслеживание дополнений, удалений и обновлений с помощью [запроса изменений](/graph/delta-query-overview) (функция [delta](../api/directoryrole-delta.md)).

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип  |Описание|
|:---------------|:--------|:----------|
|[Получение directoryRole](../api/directoryrole-get.md) | [directoryRole](directoryrole.md) |Считывание свойств и отношений объекта directoryRole.|
|[Перечисление объектов directoryRole](../api/directoryrole-list.md) | Коллекция объектов [directoryRole](directoryrole.md) | Перечисление ролей каталога, активированных в клиенте. |
|[Добавление элемента](../api/directoryrole-post-members.md) |[directoryObject](directoryobject.md)| Добавление пользователя в роль каталога путем записи данных в свойство навигации members.|
|[Список членов](../api/directoryrole-list-members.md) |Коллекция [directoryObject](directoryobject.md)| Получение пользователей, которые относятся к членам роли каталога, из свойства навигации members.|
|[Удаление члена](../api/directoryrole-delete-member.md) |[directoryObject](directoryobject.md)| Удаление ресурса user из роли каталога.|
|[Область списка — элементы роли](../api/directoryrole-list-members.md) |Коллекция [scopedRoleMembership](scopedrolemembership.md)| Перечислите членов этой роли каталога, область действия которой ограничена [административными единицами](administrativeunit.md), с помощью коллекции ресурсов scopedrolemembership изменен.|
|[delta](../api/directoryrole-delta.md)|Коллекция объектов directoryRole| Получение добавочных изменений для ролей каталога. |

## <a name="properties"></a>Свойства
| Свойство   | Тип |Описание|
|:---------------|:--------|:----------|
|description|String|Описание роли каталога. Только для чтения. |
|displayName|Строка|Отображаемое имя роли каталога. Только для чтения. |
|id|Строка|Уникальный идентификатор роли каталога. Наследуется из [directoryObject](directoryobject.md). Ключ, значение null не допускается, только для чтения.|
|roleTemplateId|String| Свойство **id** ресурса [directoryRoleTemplate](directoryroletemplate.md), определяющего значения свойств для этой роли. При активации роли каталога на клиенте следует указать свойство с помощью операции POST. После активации роли каталога свойство доступно только для чтения. |

## <a name="relationships"></a>Связи
| Связь | Тип |Описание|
|:---------------|:--------|:----------|
|members|Коллекция [directoryObject](directoryobject.md)|Пользователи, которые относятся к членам этой роли каталога. Методы HTTP: GET, POST, DELETE. Только для чтения. Допускается значение null.|
|Scopedadministrators|Коллекция [scopedRoleMembership](scopedrolemembership.md)| Члены этой роли каталога, областью действия которой являются [административные единицы](administrativeunit.md). Только для чтения. Допускается значение null.|

## <a name="json-representation"></a>Представление JSON

Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "memberOf",
    "members",
    "ownedObjects",
    "owners"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.directoryRole"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
  "roleTemplateId": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "directoryRole resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->