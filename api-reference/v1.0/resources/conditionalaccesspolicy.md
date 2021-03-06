---
title: Тип ресурса Кондитионалакцессполици
description: Представляет политику условного доступа Azure Active Directory. Политики условного доступа — это настраиваемые правила, определяющие сценарий доступа.
localization_priority: Normal
author: videor
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: ea8cfbab59acde4c6b6e2468d26e6ed9620d9652
ms.sourcegitcommit: 577bfd3bb8a2e2679ef1c5942a4a496c2aa3a277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2020
ms.locfileid: "48582326"
---
# <a name="conditionalaccesspolicy-resource-type"></a>Тип ресурса Кондитионалакцессполици

Пространство имен: microsoft.graph

Представляет политику условного доступа Azure Active Directory. Политики условного доступа — это настраиваемые правила, определяющие сценарий доступа. Дополнительные сведения см. в [документации по условному доступу](/azure/active-directory/conditional-access/).

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип | Описание |
|:-------------|:------------|:------------|
| [Список КондитионалакцессполиЦиес](../api/conditionalaccessroot-list-policies.md) | Коллекция [conditionalAccessPolicy](conditionalaccesspolicy.md) | Получение всех объектов КондитионалакцессполиЦиес в Организации. |
| [Создание Кондитионалакцессполици](../api/conditionalaccessroot-post-policies.md) | [conditionalAccessPolicy](conditionalaccesspolicy.md) | Создание нового объекта Кондитионалакцессполици. |
| [Получение Кондитионалакцессполици](../api/conditionalaccesspolicy-get.md) | [conditionalAccessPolicy](conditionalaccesspolicy.md) | Чтение свойств и связей объекта Кондитионалакцессполици. |
| [Обновление Кондитионалакцессполици](../api/conditionalaccesspolicy-update.md) | [conditionalAccessPolicy](conditionalaccesspolicy.md) | Обновление объекта Кондитионалакцессполици. |
| [Удаление Кондитионалакцессполици](../api/conditionalaccesspolicy-delete.md) | Нет | Удаление объекта Кондитионалакцессполици. |

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|conditions|[conditionalAccessConditionSet](conditionalaccessconditionset.md)| Задает правила, которые должны выполняться для применения политики. Обязательный. |
|createdDateTime|DateTimeOffset| Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`. Статического. |
|displayName|String| Задает отображаемое имя для объекта Кондитионалакцессполици. |
|грантконтролс|[conditionalAccessGrantControls](conditionalaccessgrantcontrols.md)| Указывает элементы управления предоставлением, которые должны быть выполнены для передачи политики. |
|id|String| Задает идентификатор объекта Кондитионалакцессполици. Только для чтения.|
|modifiedDateTime| DateTimeOffset|Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`. Статического. |
|сессионконтролс|[conditionalAccessSessionControls](conditionalaccesssessioncontrols.md)| Задает элементы управления сеансом, которые применяются после входа. |
|состояние|string| Задает состояние объекта Кондитионалакцессполици. Возможные значения: `enabled`, `disabled`, `enabledForReportingButNotEnforced`. Обязательный. |

## <a name="relationships"></a>Связи

Отсутствуют.

## <a name="json-representation"></a>Представление в формате JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "displayName",
    "sessionControls",
    "grantControls"
  ],
  "@odata.type": "microsoft.graph.conditionalAccessPolicy",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "conditions": {"@odata.type": "microsoft.graph.conditionalAccessConditionSet"},
  "createdDateTime": "String (timestamp)",
  "displayName": "String",
  "grantControls": {"@odata.type": "microsoft.graph.conditionalAccessGrantControls"},
  "id": "String (identifier)",
  "modifiedDateTime": "String (timestamp)",
  "sessionControls": {"@odata.type": "microsoft.graph.conditionalAccessSessionControls"},
  "state": "string"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conditionalAccessPolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->