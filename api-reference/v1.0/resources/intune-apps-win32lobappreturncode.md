---
title: Тип ресурса win32LobAppReturnCode
description: Содержит свойства кода возврата для приложения Win32
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: e9b64542a7c3679e31b23ee63bcdcf9713bccc92
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48036760"
---
# <a name="win32lobappreturncode-resource-type"></a>Тип ресурса win32LobAppReturnCode

Пространство имен: microsoft.graph

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Содержит свойства кода возврата для приложения Win32

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|ретурнкоде|Int32|Возвращаемый код.|
|type|[win32LobAppReturnCodeType](../resources/intune-apps-win32lobappreturncodetype.md)|Тип кода возврата. Возможные значения: `failed`, `success`, `softReboot`, `hardReboot`, `retry`.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppReturnCode"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppReturnCode",
  "returnCode": 1024,
  "type": "String"
}
```





