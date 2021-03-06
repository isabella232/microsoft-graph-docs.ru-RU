---
title: Тип ресурса Девицехеалсскриптинтежерпараметер
description: Свойства целого параметра скрипта.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 6ebc614c93e88d01503c0219200598148c7b84cc
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49226491"
---
# <a name="devicehealthscriptintegerparameter-resource-type"></a>Тип ресурса Девицехеалсскриптинтежерпараметер

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Свойства целого параметра скрипта.


Наследуется от [девицехеалсскриптпараметер](../resources/intune-devices-devicehealthscriptparameter.md)

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|name|String|Имя параметра, унаследованного от [девицехеалсскриптпараметер](../resources/intune-devices-devicehealthscriptparameter.md)|
|description|String|Описание параметра, унаследованного от [девицехеалсскриптпараметер](../resources/intune-devices-devicehealthscriptparameter.md)|
|isRequired|Boolean|Является ли параметр должен наследоваться от [девицехеалсскриптпараметер](../resources/intune-devices-devicehealthscriptparameter.md)|
|апплидефаултвалуевхеннотассигнед|Boolean|Применяется ли значение DefaultValue при отсутствии назначенного наследования от [девицехеалсскриптпараметер](../resources/intune-devices-devicehealthscriptparameter.md)|
|Значение|Int32|Значение по умолчанию параметра Integer. Допустимые значения: от 2147483648 до 2147483647|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceHealthScriptIntegerParameter"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceHealthScriptIntegerParameter",
  "name": "String",
  "description": "String",
  "isRequired": true,
  "applyDefaultValueWhenNotAssigned": true,
  "defaultValue": 1024
}
```




