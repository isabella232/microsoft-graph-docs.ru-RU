---
title: Тип ресурса allDevicesAssignmentTarget
description: Представляет ресурс, назначенный всем управляемым устройствам в клиенте.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 7f583f89f8ef3213f980b082cb6b15747722142b
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49306949"
---
# <a name="alldevicesassignmenttarget-resource-type"></a>Тип ресурса allDevicesAssignmentTarget

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Представляет ресурс, назначенный всем управляемым устройствам в клиенте.


Наследуется от ресурса [deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|девицеандаппманажементассигнментфилтерид|String|Идентификатор фильтра для назначения назначения. Наследуется от [девицеандаппманажементассигнменттаржет](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|
|deviceAndAppManagementAssignmentFilterType|[deviceAndAppManagementAssignmentFilterType](../resources/intune-shared-deviceandappmanagementassignmentfiltertype.md)|Тип фильтра целевого назначения, например, Exclude или include. Наследуется от [девицеандаппманажементассигнменттаржет](../resources/intune-shared-deviceandappmanagementassignmenttarget.md). Возможные значения: `none`, `include`.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.allDevicesAssignmentTarget"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.allDevicesAssignmentTarget",
  "deviceAndAppManagementAssignmentFilterId": "String",
  "deviceAndAppManagementAssignmentFilterType": "String"
}
```




