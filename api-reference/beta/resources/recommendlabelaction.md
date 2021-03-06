---
title: Тип ресурса Рекоммендлабелактион
description: Представляет метку, которая должна быть рекомендована пользователю для приложения в файл на основе типов конфиденциальной информации.
localization_priority: Normal
author: tommoser
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: b5deebaec460bd8c1993cc0c308e68e6f6f986a9
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48055186"
---
# <a name="recommendlabelaction-resource-type"></a>Тип ресурса Рекоммендлабелактион

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет метку, которая должна быть рекомендована пользователю для приложения в файл на основе обнаруженных типов конфиденциальной информации. [Евалуатеклассификатионресултс](../api/informationprotectionlabel-evaluateClassificationResults.md) может возвращать **рекоммендлабелактион** , если для политики метки Microsoft Information Protection задано значение **рекомендовать** и подпись, а не задано применение метки. Пользователь или апплиатион может игнорировать или принять рекомендацию. 

## <a name="properties"></a>Свойства

| Свойство                    | Тип                                                                     | Описание                                                           |
| :-------------------------- | :----------------------------------------------------------------------- | :-------------------------------------------------------------------- |
| актионсаурце                | String                                                                   | Возможные значения: `manual`, `automatic`, `recommended`, `default`. |
| actions                     | Коллекция [информатионпротектионактион](informationprotectionaction.md) | Действия, которые необходимо выполнить, если пользователь принимает метку.                                                                       |
| label                       | [лабелдетаилс](labeldetails.md)                                          | Рекомендуемая метка.                                                                      |
| респонсиблесенситиветипеидс | Коллекция объектов Guid                                                          | Идентификаторы GUID типа конфиденциальной информации, которые привели к выдано рекомендация.                                                                      |

## <a name="json-representation"></a>Представление в формате JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recommendLabelAction",
  "baseType": "microsoft.graph.informationProtectionAction"
}-->

```json
{
  "actionSource": "String",
  "actions": [{"@odata.type": "microsoft.graph.informationProtectionAction"}],
  "label": {"@odata.type": "microsoft.graph.labelDetails"},
  "responsibleSensitiveTypeIds": ["Guid"]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recommendLabelAction resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


