---
title: Тип ресурса Девицеманажементскриптрунсуммари
description: Содержит свойства сводки по запуску сценария управления устройствами.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 3854cf7730326e1b291863416d09915ccf7b4d2a
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49267609"
---
# <a name="devicemanagementscriptrunsummary-resource-type"></a>Тип ресурса Девицеманажементскриптрунсуммари

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Содержит свойства сводки по запуску сценария управления устройствами.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Получение Девицеманажементскриптрунсуммари](../api/intune-devices-devicemanagementscriptrunsummary-get.md)|[deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md);|Чтение свойств и связей объекта [девицеманажементскриптрунсуммари](../resources/intune-devices-devicemanagementscriptrunsummary.md) .|
|[Обновление Девицеманажементскриптрунсуммари](../api/intune-devices-devicemanagementscriptrunsummary-update.md)|[deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md);|Обновление свойств объекта [девицеманажементскриптрунсуммари](../resources/intune-devices-devicemanagementscriptrunsummary.md) .|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Key объекта сводки запуска сценария управления устройствами. Это свойство доступно только для чтения.|
|сукцессдевицекаунт|Int32|Число устройств для успешной попытки.|
|errorDeviceCount|Int32|Количество устройств с ошибками.|
|сукцессусеркаунт|Int32|Число пользователей Success.|
|errorUserCount|Int32|Количество пользователей с ошибками.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementScriptRunSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementScriptRunSummary",
  "id": "String (identifier)",
  "successDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "successUserCount": 1024,
  "errorUserCount": 1024
}
```




