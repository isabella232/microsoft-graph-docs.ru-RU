---
title: Тип ресурса ПрожектпартиЦипатион
description: Тип ресурса ПрожектпартиЦипатион
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: resourcePageType
ms.openlocfilehash: 465a45a2ba8a607d0537e66b96207b3d60626517
ms.sourcegitcommit: dd94c3a0f7663699825b6dbc119cdcef494cd130
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2019
ms.locfileid: "37950474"
---
# <a name="projectparticipation-resource-type"></a>Тип ресурса ПрожектпартиЦипатион

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет подробные сведения о проектах, связанных с пользователем.

Наследуется от [итемфацет](itemfacet.md).

## <a name="methods"></a>Методы

| Метод                                                         | Возвращаемый тип                                     | Описание                                                       |
|:---------------------------------------------------------------|:------------------------------------------------|:------------------------------------------------------------------|
| [Получение ПрожектпартиЦипатион](../api/projectparticipation-get.md) | [прожектпартиЦипатион](projectparticipation.md) | Чтение свойств и связей объекта **прожектпартиЦипатион** . |
| [Обновление ПрожектпартиЦипатион](../api/projectparticipation-update.md)                | [прожектпартиЦипатион](projectparticipation.md) | Обновление объекта **прожектпартиЦипатион** .                               |
| [Удаление ПрожектпартиЦипатион](../api/projectparticipation-delete.md)                | Нет.                                            | Удаление объекта **прожектпартиЦипатион** .                               |

## <a name="properties"></a>Свойства

| Свойство     | Тип                                        | Описание                                                                                      |
|:-------------|:--------------------------------------------|:-------------------------------------------------------------------------------------------------|
|categories    | Коллекция String                           | Содержит категории, связанные с проектом пользователем (например, цифровое преобразование, гидростенд). |
|Клиенты        |[компанидетаил](companydetail.md)            | Содержит подробные сведения о клиенте, для которого выполнялся проект.                              |
|коллег    |Коллекция [релатедперсон](relatedperson.md) | Список людей, которые также работали над проектом.                                                          |
|описаны        |[поситиондетаил](positiondetail.md)          | Содержит подробные сведения о роли пользователя в проекте.                                             |
|displayName   |String                                       |Содержит понятное имя проекта.                                                         |
|спонсорами      |Коллекция [релатедперсон](relatedperson.md) | Пользователь или люди, которые спонсорируют проект.                                                         |

## <a name="relationships"></a>Связи

Отсутствуют.

## <a name="json-representation"></a>Представление в формате JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.projectParticipation",
  "baseType": ""
}-->

```json
{
  "categories": ["String"],
  "client": {"@odata.type": "microsoft.graph.companyDetail"},
  "colleagues": [{"@odata.type": "microsoft.graph.relatedPerson"}],
  "detail": {"@odata.type": "microsoft.graph.positionDetail"},
  "displayName": "String",
  "sponsors": [{"@odata.type": "microsoft.graph.relatedPerson"}]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "projectParticipation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->