---
author: JeremyKelley
description: Представляет сведения о итеративном процессе для отправки больших файлов в OneDrive, OneDrive для бизнеса или библиотеки документов SharePoint, а также в виде вложений файлов в события и объекты сообщений Outlook.
title: Тип ресурса uploadSession
localization_priority: Normal
doc_type: resourcePageType
ms.prod: non-product-specific
ms.openlocfilehash: 64c907559337a1e6c5f40e046726c747751aaf03
ms.sourcegitcommit: 3b9eb50b790d952c7f350433ef7531d5e6d4b963
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2020
ms.locfileid: "48723723"
---
# <a name="uploadsession-resource-type"></a>Тип ресурса uploadSession

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет сведения о итеративном процессе для отправки больших файлов в:

- OneDrive
- OneDrive для бизнеса
- Библиотеки документов SharePoint
- [События](event.md) и элементы [сообщений](message.md) Outlook в виде вложений
- Элементы универсального принтера [printDocument](printdocument.md)

## <a name="json-representation"></a>Представление JSON

Ниже показано представление JSON ресурса.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "uploadUrl", "nextExpectedRanges" ],
  "@odata.type": "microsoft.graph.uploadSession",
  "baseType": null
}-->

```json
{
  "uploadUrl": "String",
  "expirationDateTime": "String (timestamp)",
  "nextExpectedRanges": ["String"]
}
```

## <a name="properties"></a>Свойства


| Свойство       | Тип              |Описание
|:-------------------|:------------------|:------------------------------------
| expirationDateTime | DateTimeOffset    | Дата и время (в формате UTC) истечения срока действия сеанса. Полный файл необходимо отправить до наступления этого момента.
| nextExpectedRanges | Коллекция строк | При отправке файлов в библиотеки документов это коллекция диапазонов байтов, которые сервер отсутствует для файла. Эти диапазоны обозначаются нулевым индексом и форматом "{Start}-{End}" (например, "0-26", чтобы указать первые 27 байтов файла). При отправке файлов в виде вложений Outlook вместо коллекции диапазонов это свойство всегда указывает на одно значение "{Start}", расположение в файле, в котором должна начаться следующая загрузка.
| uploadUrl          | Строка            | URL-адрес конечной точки, принимающей запросы PUT для диапазонов байтов файла.

## <a name="see-also"></a>См. также

- [Присоединение больших файлов к сообщениям и событиям Outlook в качестве вложений ](/graph/outlook-large-attachments)
- [Отправка больших файлов с помощью сеанса отправки](../api/driveitem-createuploadsession.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "UploadSession is used to provide information about large file uploads.",
  "section": "documentation",
  "tocPath": "Resources/UploadSession",
  "suppressions": []
}
-->


