---
title: Тип ресурса Макоссистемекстенсион
description: Представляет определенное расширение системы macOS.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 8cea7fb3cb7c0c95fb0ad5174b171bc1993aa1fb
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49294027"
---
# <a name="macossystemextension-resource-type"></a>Тип ресурса Макоссистемекстенсион

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Представляет определенное расширение системы macOS.

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|теамидентифиер|String|Получает или задает идентификатор группы, использованный для подписи расширения системы.|
|bundleId|String|Получает или задает идентификатор пакета расширения системы.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.macOSSystemExtension"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSSystemExtension",
  "teamIdentifier": "String",
  "bundleId": "String"
}
```




