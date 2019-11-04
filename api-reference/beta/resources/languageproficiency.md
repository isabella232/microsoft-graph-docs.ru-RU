---
title: Тип ресурса ЛангуажепрофиЦиенци
description: Тип ресурса ЛангуажепрофиЦиенци
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: resourcePageType
ms.openlocfilehash: 3a022d9c255bbfee03ef7f1fec891bc0fa757480
ms.sourcegitcommit: dd94c3a0f7663699825b6dbc119cdcef494cd130
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2019
ms.locfileid: "37950460"
---
# <a name="languageproficiency-resource-type"></a>Тип ресурса ЛангуажепрофиЦиенци

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет подробные сведения о языках, добавленных пользователем в свой [профиль](profile.md).

Наследуется от [итемфацет](itemFacet.md).

## <a name="methods"></a>Методы

| Метод                                                       | Возвращаемый тип                                   | Описание                                                      | 
|:-------------------------------------------------------------|:----------------------------------------------|:-----------------------------------------------------------------|
| [Получение ЛангуажепрофиЦиенци](../api/languageproficiency-get.md) | [лангуажепрофиЦиенци](languageproficiency.md) | Чтение свойств и связей объекта **лангуажепрофиЦиенци** . |
| [Обновление ЛангуажепрофиЦиенци](../api/languageproficiency-update.md)               | [лангуажепрофиЦиенци](languageproficiency.md) | Обновление объекта **лангуажепрофиЦиенци** .                               |
| [Удаление ЛангуажепрофиЦиенци](../api/languageproficiency-delete.md)               | Нет.                                          | Удаление объекта **лангуажепрофиЦиенци** .                               |

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание                                                                                                                                                 |
|:-------------|:------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
|displayName   |String       | Содержит имя языка в длинном формате.                                                                                                   |
|навыки   |string       | Возможные значения: `elementary`, `conversational`, `limitedWorking`, `professionalWorking`, `fullProfessional`, `nativeOrBilingual`, `unknownFutureValue`.|
|tag           |String       | Содержит четырехзначный BCP47 Name для языка (EN-US, No-NetBIOS, en-AU).                                                                                  |

## <a name="relationships"></a>Связи

Отсутствуют.

## <a name="json-representation"></a>Представление в формате JSON

Ниже указано представление ресурса в формате JSON. 

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.languageProficiency",
  "baseType": ""
}-->

```json
{
  "displayName": "String",
  "proficiency": "string",
  "tag": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "languageProficiency resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->