---
title: Тип ресурса Едукатионалактивити
description: Тип ресурса Едукатионалактивити
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: resourcePageType
ms.openlocfilehash: 8d060de55d765adb7e01e6b03842c569f03c8d4f
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "37939623"
---
# <a name="educationalactivity-resource-type"></a>Тип ресурса Едукатионалактивити

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет данные, которые пользователь предоставил, относящихся к выпуску, выпускнику, выпуску или другим учебным действиям.

Наследует свойства метаданных от [итемфацет](itemfacet.md).

## <a name="methods"></a>Методы

| Метод                                                       | Возвращаемый тип                                   | Описание                                                      |
|:-------------------------------------------------------------|:----------------------------------------------|:-----------------------------------------------------------------|
| [Получение Едукатионалактивити](../api/educationalactivity-get.md) | [едукатионалактивити](educationalactivity.md) | Чтение свойств и связей объекта Едукатионалактивити. |
| [Update](../api/educationalactivity-update.md)               | [едукатионалактивити](educationalactivity.md) | Обновление объекта Едукатионалактивити.                               |
| [Delete](../api/educationalactivity-delete.md)               | Нет.                                          | Удаление объекта Едукатионалактивити.                               |

## <a name="properties"></a>Свойства

| Свойство           | Тип                                                      | Описание                                                                |
|:-------------------|:----------------------------------------------------------|:---------------------------------------------------------------------------|
|комплетионмонсеар |Дата                                                       |Месяц и год, когда пользователь выполнит или выполнил действие.            |
|ендмонсеар        |Дата                                                       |Месяц и год, когда пользователь завершил действие учебного заведения.  |
|Организация         |[институтиондата](institutiondata.md)                      |Содержит подробные сведения о учебном заведения.                             |
|Программа             |[едукатионалактивитидетаил](educationalactivitydetail.md)  |Содержит расширенные сведения о программе или курсе.                  |
|стартмонсеар      |Дата                                                       |Месяц и год, когда пользователь присвоено указанному действию.              |

## <a name="relationships"></a>Связи

Нет

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationalActivity",
  "baseType": ""
}-->

```json
{
  "completionMonthYear": "String (timestamp)",
  "endMonthYear": "String (timestamp)",
  "institution": {"@odata.type": "microsoft.graph.institutionData"},
  "program": {"@odata.type": "microsoft.graph.educationalActivityDetail"},
  "startMonthYear": "String (timestamp)"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationalActivity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->