---
title: Тип ресурса appRoleAssignment
description: Используется, чтобы записать, когда пользователю, группе или субъекту-службе присваивается роль приложения в субъекте-службе приложения. Можно создавать, читать и удалять назначения ролей приложений.
localization_priority: Priority
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: psignoret
ms.openlocfilehash: c23c0a9d4e3f41ca21b285eb7f5484678c3d8b66
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "48405626"
---
# <a name="approleassignment-resource-type"></a>Тип ресурса appRoleAssignment

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Используется, чтобы записать, когда пользователю, группе или субъекту-службе присваивается роль приложения для какого-либо приложения.

Назначение роли приложения — это отношение между назначенным субъектом (пользователь, группа или субъект-служба), приложением ресурса (субъект-служба приложения) и ролью приложения, определенной для приложения ресурса.

Если у [роли приложения](approle.md), которая назначена субъекту, есть непустое свойство **value**, оно включается в утверждения **ролей** маркеров, где субъектом может быть назначенный субъект (например, отклики SAML, маркеры идентификаторов, маркеры доступа, определяющие вошедшего в систему пользователя, или маркер доступа, определяющий субъект-службу). Приложения и API используют эти утверждения в логике авторизации.

Пользователю можно назначить роль приложения напрямую. Если роль приложения назначена группе, то эта роль приложения также считается назначенной непосредственным участникам этой группы. Когда пользователю назначается роль приложения для какого-либо приложения, название этого приложения отображается на [портале "Мои приложения](/azure/active-directory/user-help/my-apps-portal-end-user-access) этого пользователя и в [средстве запуска приложений Microsoft 365](https://support.office.com/article/meet-the-office-365-app-launcher-79f12104-6fed-442f-96a0-eb089a3f476a).

Если назначенный субъект является субъектом-службой, то предоставляется [доступ только к приложению](/azure/active-directory/develop/v2-permissions-and-consent#permission-types). Когда пользователь или администратор принимает разрешение с доступом только к приложению, создается назначение роли приложения, в котором назначенный субъект является субъектом-службой для приложения клиента, а ресурс является субъектом-службой целевого API.

## <a name="properties"></a>Свойства

| Свойство | Тип | Описание |
|:---------------|:--------|:----------|
| id | Строка | Уникальный идентификатор ключа **appRoleAssignment**. Значение null не допускается. Только для чтения. |
| creationTimestamp | DateTimeOffset | Время создания назначения роли приложения. Тип Timestamp представляет сведения о времени и дате в формате ISO 8601 (всегда используется время в формате UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`. Только для чтения. Не поддерживает `$filter`. |
| principalId | Guid | Уникальный идентификатор (**ИД**) [пользователя](user.md), [группы](group.md) или [субъекта-службы](serviceprincipal.md), которым предоставляется роль приложения. Требуется при создании. Не поддерживает `$filter`. |
| principalType | Строка | Тип назначенного субъекта. Это может "Пользователь", "Группа" или "Субъект-служба". Только для чтения. Не поддерживает `$filter`. |
| principalDisplayName | Строка |Отображаемое имя пользователя, группа или субъекта-службы, которым было предоставлено назначение роли приложения. Только для чтения. Поддерживает `$filter` (`eq` и `startswith`). |
| resourceId | Guid |Уникальный идентификатор (**ИД**) ресурса [субъект-служба](serviceprincipal.md), для которого производится назначение. Требуется при создании. Поддерживает `$filter` (только `eq`). |
| resourceDisplayName | Строка | Отображаемое имя субъекта-службы приложения ресурса, для которого производится назначение. Не поддерживает `$filter`. |
| appRoleId | Guid | Идентификатор (**ИД**) [роли приложения](approle.md), которая назначается субъекту. Эта роль приложения должна предоставляться в свойстве **appRoles** субъекта-службы приложения ресурса (**resourceId**). Если в приложении ресурса не объявлены никакие роли приложения, можно указать ИД роли приложения по умолчанию (`00000000-0000-0000-0000-000000000000`), чтобы указать, что субъект назначен приложению ресурса без каких-либо определенных ролей приложения. Требуется при создании. Не поддерживает `$filter`. |

## <a name="json-representation"></a>Представление JSON

Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.appRoleAssignment"
}-->

```json
{
  "id": "string",
  "creationTimestamp": "String (timestamp)",
  "principalDisplayName": "string",
  "principalId": "guid",
  "principalType": "string",
  "resourceDisplayName": "string",
  "resourceId": "guid",
  "appRoleId": "guid"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "appRoleAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->