---
title: Тип ресурса Кондитионалакцесссессионконтролс
description: Представляет сложный тип элементов управления сеанса, который принудительно применяется после входа.
localization_priority: Normal
author: videor
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 78c9ab3c3b5a55623ba13e1f7ce6d28a9425ded5
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48057012"
---
# <a name="conditionalaccesssessioncontrols-resource-type"></a>Тип ресурса Кондитионалакцесссессионконтролс

Пространство имен: microsoft.graph

Представляет элементы управления сеансом, которые применяются после входа.
Все элементы управления сеансом наследуются от [кондитионалакцесссессионконтрол](conditionalaccesssessioncontrol.md).

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|аппликатионенфорцедрестриктионс|[applicationEnforcedRestrictionsSessionControl](applicationenforcedrestrictionssessioncontrol.md)| Управление сеансами для применения ограничений приложений. Этот элемент управления сеансом поддерживают только Exchange Online и SharePoint Online. |
|клаудаппсекурити|[cloudAppSecuritySessionControl](cloudappsecuritysessioncontrol.md)| Управление сеансами для применения Cloud App Security.|
|персистентбровсер|[persistentBrowserSessionControl](persistentbrowsersessioncontrol.md)| Элемент управления сеансом, чтобы определить, следует ли сохранять файлы cookie. Для правильной работы этого элемента управления сеансом необходимо выбрать все приложения. |
|сигнинфрекуенци|[signInFrequencySessionControl](signinfrequencysessioncontrol.md)| Управление сеансами для применения частоты входа.|

## <a name="relationships"></a>Связи

Отсутствуют.

## <a name="json-representation"></a>Представление в формате JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "applicationEnforcedRestrictions",
    "persistentBrowser",
    "cloudAppSecurity",
    "signInFrequency"
  ],
  "@odata.type": "microsoft.graph.conditionalAccessSessionControls",
  "baseType": null
}-->

```json
{
  "applicationEnforcedRestrictions": {"@odata.type": "microsoft.graph.applicationEnforcedRestrictionsSessionControl"},
  "cloudAppSecurity": {"@odata.type": "microsoft.graph.cloudAppSecuritySessionControl"},
  "persistentBrowser": {"@odata.type": "microsoft.graph.persistentBrowserSessionControl"},
  "signInFrequency": {"@odata.type": "microsoft.graph.signInFrequencySessionControl"}
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conditionalAccessSessionControls resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

