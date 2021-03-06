---
title: Тип ресурса Кондитионалакцесскондитионсет
description: Представляет тип условий, определяющих, когда применяется политика.
localization_priority: Normal
author: videor
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: ba88e9e5fd67bba5dd88fe323f3140bdbebff479
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47994297"
---
# <a name="conditionalaccessconditionset-resource-type"></a>Тип ресурса Кондитионалакцесскондитионсет

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет тип условий, определяющих, когда применяется политика.

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|заявлен|[conditionalAccessApplications](conditionalaccessapplications.md)| Приложения и действия пользователя, включенные в политику и исключенные из нее. Обязательно. |
|users|[conditionalAccessUsers](conditionalaccessusers.md)| Пользователи, группы и роли, включенные в политику и исключенные из нее. Обязательно. |
|клиентапптипес|Коллекция String| Типы клиентских приложений, включенные в политику. Возможные значения: `all`, `browser`, `mobileAppsAndDesktopClients`, `exchangeActiveSync`, `easSupported`, `other`.|
|deviceStates|[conditionalAccessDeviceStates](conditionalaccessdevicestates.md)| Состояния устройств в политике. |
|драйверов|[кондитионалакцессдевицес](conditionalaccessdevices.md)| Устройства в политике. |
|locations|[conditionalAccessLocations](conditionalaccesslocations.md)| Расположения, включенные в политику и исключенные из нее. |
|Embedded|[conditionalAccessPlatforms](conditionalaccessplatforms.md)| Платформы, включенные в политику и исключенные из нее. |
|сигнинрисклевелс|Коллекция String| Уровни риска входа, включенные в политику. Возможные значения: `low`, `medium`, `high`, `none`.|
|усеррисклевелс|Коллекция String| Уровни риска пользователей, включенные в политику. Возможные значения: `low`, `medium`, `high`, `none`.|

>**Примечание.** 

>**клиентапптипе** `modern` считается устаревшим и заменяется на `mobileAppsAndDesktopClients` . 

>**клиентапптипе** `easUnsupported` считается нерекомендуемым, в том `exchangeActiveSync` числе поддерживаемых и неподдерживаемых платформах EAS. 

>Мы рекомендуем использовать условие **девицестатес** , и оно может быть удалено в будущем. Перемотка вперед, используйте состояние **Devices** .

## <a name="relationships"></a>Связи

Отсутствуют.

## <a name="json-representation"></a>Представление в формате JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "clientAppTypes",
    "deviceStates",
    "devices",
    "locations",
    "platforms",
    "signInRiskLevels"
  ],
  "@odata.type": "microsoft.graph.conditionalAccessConditionSet",
  "baseType": null
}-->

```json
{
  "applications": {"@odata.type": "microsoft.graph.conditionalAccessApplications"},
  "users": {"@odata.type": "microsoft.graph.conditionalAccessUsers"},
  "clientAppTypes": ["String"],
  "deviceStates": {"@odata.type": "microsoft.graph.conditionalAccessDeviceStates"},
  "devices": {"@odata.type": "microsoft.graph.conditionalAccessDevices"},
  "locations": {"@odata.type": "microsoft.graph.conditionalAccessLocations"},
  "platforms": {"@odata.type": "microsoft.graph.conditionalAccessPlatforms"},
  "signInRiskLevels": ["String"]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conditionalAccessConditionset resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


