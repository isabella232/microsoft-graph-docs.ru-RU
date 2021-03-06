---
title: Тип ресурса Макосминимумоператингсистем
description: Минимальная операционная система, необходимая для приложения MacOS.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 20a08b6be50608bebf4482e61f032b9587b04566
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49281770"
---
# <a name="macosminimumoperatingsystem-resource-type"></a>Тип ресурса Макосминимумоператингсистем

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Минимальная операционная система, необходимая для приложения MacOS.

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|v10_7|Boolean|Mac OS 10,7 или более поздней версии.|
|v10_8|Boolean|Mac OS 10,8 или более поздней версии.|
|v10_9|Boolean|Mac OS 10,9 или более поздней версии.|
|v10_10|Boolean|Mac OS 10,10 или более поздней версии.|
|v10_11|Boolean|Mac OS 10,11 или более поздней версии.|
|v10_12|Boolean|Mac OS 10,12 или более поздней версии.|
|v10_13|Boolean|Mac OS 10,13 или более поздней версии.|
|v10_14|Boolean|Mac OS 10,14 или более поздней версии.|
|v10_15|Boolean|Mac OS 10,15 или более поздней версии.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.macOSMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSMinimumOperatingSystem",
  "v10_7": true,
  "v10_8": true,
  "v10_9": true,
  "v10_10": true,
  "v10_11": true,
  "v10_12": true,
  "v10_13": true,
  "v10_14": true,
  "v10_15": true
}
```




