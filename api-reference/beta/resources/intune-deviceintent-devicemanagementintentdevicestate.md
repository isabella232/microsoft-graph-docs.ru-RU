---
title: Тип ресурса Девицеманажементинтентдевицестате
description: Объект, представляющий состояние устройства для намерения
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 6a13f6341cd953f4142037059d9d96a81c3199f2
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49275792"
---
# <a name="devicemanagementintentdevicestate-resource-type"></a>Тип ресурса Девицеманажементинтентдевицестате

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Объект, представляющий состояние устройства для намерения

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список Девицеманажементинтентдевицестатес](../api/intune-deviceintent-devicemanagementintentdevicestate-list.md)|Коллекция [девицеманажементинтентдевицестате](../resources/intune-deviceintent-devicemanagementintentdevicestate.md)|Список свойств и связей объектов [девицеманажементинтентдевицестате](../resources/intune-deviceintent-devicemanagementintentdevicestate.md) .|
|[Получение Девицеманажементинтентдевицестате](../api/intune-deviceintent-devicemanagementintentdevicestate-get.md)|[deviceManagementIntentDeviceState](../resources/intune-deviceintent-devicemanagementintentdevicestate.md)|Чтение свойств и связей объекта [девицеманажементинтентдевицестате](../resources/intune-deviceintent-devicemanagementintentdevicestate.md) .|
|[Создание Девицеманажементинтентдевицестате](../api/intune-deviceintent-devicemanagementintentdevicestate-create.md)|[deviceManagementIntentDeviceState](../resources/intune-deviceintent-devicemanagementintentdevicestate.md)|Создание нового объекта [девицеманажементинтентдевицестате](../resources/intune-deviceintent-devicemanagementintentdevicestate.md) .|
|[Удаление Девицеманажементинтентдевицестате](../api/intune-deviceintent-devicemanagementintentdevicestate-delete.md)|Нет|Удаляет объект [девицеманажементинтентдевицестате](../resources/intune-deviceintent-devicemanagementintentdevicestate.md).|
|[Обновление Девицеманажементинтентдевицестате](../api/intune-deviceintent-devicemanagementintentdevicestate-update.md)|[deviceManagementIntentDeviceState](../resources/intune-deviceintent-devicemanagementintentdevicestate.md)|Обновление свойств объекта [девицеманажементинтентдевицестате](../resources/intune-deviceintent-devicemanagementintentdevicestate.md) .|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Идентификатор|
|userPrincipalName|String|Имя участника-пользователя, сообщаемое на устройстве|
|userName|String|Имя пользователя, сообщаемое на устройстве|
|deviceDisplayName|String|Имя устройства, о котором сообщается|
|lastReportedDateTime|DateTimeOffset|Дата и время последнего изменения отчета о намерениях|
|state|[комплианцестатус](../resources/intune-shared-compliancestatus.md)|Состояние устройства для цели. Возможные значения: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.|
|deviceId|String|Идентификатор устройства, о котором сообщается|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementIntentDeviceState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementIntentDeviceState",
  "id": "String (identifier)",
  "userPrincipalName": "String",
  "userName": "String",
  "deviceDisplayName": "String",
  "lastReportedDateTime": "String (timestamp)",
  "state": "String",
  "deviceId": "String"
}
```




