---
title: Тип ресурса meetingTimeSuggestionsResult
description: Коллекция предложений собраний, если таковая существует, и причина в отсутствии.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
doc_type: resourcePageType
ms.openlocfilehash: e12bcb2e75a85b33f0968d13b9f9a38dbc026cfe
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47971617"
---
# <a name="meetingtimesuggestionsresult-resource-type"></a>Тип ресурса meetingTimeSuggestionsResult

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Коллекция предложений собраний, если таковая существует, и причина в отсутствии.

Ниже представлены возможные причины, по которым метод [findMeetingTimes](../api/user-findmeetingtimes.md) может не возвращать предложения.

|**Значение emptySuggestionsReason**|**Причины**|
|:-----|:-----|
| аттендисунаваилабле | Все сведения о доступности участников известны, но недостаточно участников для [достижения порогового значения, которое](../api/user-findmeetingtimes.md#the-confidence-of-a-meeting-suggestion) составляет 50% по умолчанию для любого периода времени.|
| аттендисунаваилаблеорункновн | Отсутствуют сведения о доступности некоторых или всех участников, из-за чего значение достоверности собрания становится ниже заданного порога (значение по умолчанию — 50 %). Доступность участника может стать неизвестной, если он находится за пределами организации или произошла ошибка при получении сведений о доступности.|
| локатионсунаваилабле | Для свойства **Required** параметра **locationConstraint** задано значение true, но в вычисляемых интервалах времени нет доступных расположений. |
| организерунаваилабле | Для параметра **isOrganizerOptional** задано значение false, но организатор недоступен в запрашиваемый период времени. |
| unknown | Причина отсутствия предложений неизвестна.|

## <a name="json-representation"></a>Представление JSON

Ниже показано представление JSON ресурса.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingTimeSuggestionsResult"
}-->

```json
{
  "emptySuggestionsReason": "String",
  "meetingTimeSuggestions": [{"@odata.type": "microsoft.graph.meetingTimeSuggestion"}]
}

```
## <a name="properties"></a>Свойства
| Свойство     | Тип   |Описание|
|:---------------|:--------|:----------|
|емптисугжестионсреасон|String|Причина отсутствия предложений в результатах. Возможные значения: `attendeesUnavailable`, `attendeesUnavailableOrUnknown`, `locationsUnavailable`, `organizerUnavailable` и `unknown`. Это свойство представляет собой пустую строку, если в свойстве **митингтимесугжестионс** есть предложения о собраниях.|
|митингтимесугжестионс|Коллекция объектов [meetingTimeSuggestion](meetingtimesuggestion.md)|Массив предложений.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "meetingTimeSuggestionsResult resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


