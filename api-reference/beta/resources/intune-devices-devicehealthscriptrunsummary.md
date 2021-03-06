---
title: Тип ресурса Девицехеалсскриптрунсуммари
description: Содержит свойства сводки по запуску сценария управления устройствами.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: ef09482999fdff50ebbd1bd0e0df5320aad6f206
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49299361"
---
# <a name="devicehealthscriptrunsummary-resource-type"></a>Тип ресурса Девицехеалсскриптрунсуммари

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Содержит свойства сводки по запуску сценария управления устройствами.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Получение Девицехеалсскриптрунсуммари](../api/intune-devices-devicehealthscriptrunsummary-get.md)|[deviceHealthScriptRunSummary](../resources/intune-devices-devicehealthscriptrunsummary.md)|Чтение свойств и связей объекта [девицехеалсскриптрунсуммари](../resources/intune-devices-devicehealthscriptrunsummary.md) .|
|[Обновление Девицехеалсскриптрунсуммари](../api/intune-devices-devicehealthscriptrunsummary-update.md)|[deviceHealthScriptRunSummary](../resources/intune-devices-devicehealthscriptrunsummary.md)|Обновление свойств объекта [девицехеалсскриптрунсуммари](../resources/intune-devices-devicehealthscriptrunsummary.md) .|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Ключевой объект сводки запуска сценария работоспособности устройства. Это свойство доступно только для чтения.|
|ноиссуедетектеддевицекаунт|Int32|Количество устройств, для которых сценарий обнаружения не обнаружил проблему, и устройство находится в работоспособном состоянии.|
|иссуедетектеддевицекаунт|Int32|Количество устройств, для которых обнаружена ошибка сценария обнаружения|
|детектионскриптеррордевицекаунт|Int32|Количество устройств, на которых возникла ошибка при выполнении сценария обнаружения и который не был выполнен|
|детектионскриптпендингдевицекаунт|Int32|Количество устройств, на которых еще не выполнялась последняя версия сценария работоспособности устройства|
|иссуеремедиатеддевицекаунт|Int32|Количество устройств, для которых сценарий исправления мог разрешить обнаруженную проблему|
|ремедиатионскиппеддевицекаунт|Int32|Количество устройств, для которых было пропущено исправление|
|иссуереоккурреддевицекаунт|Int32|Количество устройств, для которых сценарий исправления успешно выполнен, но не удалось разрешить обнаруженную проблему|
|ремедиатионскриптеррордевицекаунт|Int32|Количество устройств, для которых при выполнении сценария исправления возникла ошибка и оно не было завершено|
|ластскриптрундатетиме|DateTimeOffset|Время последнего запуска сценария на всех устройствах|
|иссуеремедиатедкумулативедевицекаунт|Int32|Количество устройств, которые были исправлены за последние 30 дней|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceHealthScriptRunSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceHealthScriptRunSummary",
  "id": "String (identifier)",
  "noIssueDetectedDeviceCount": 1024,
  "issueDetectedDeviceCount": 1024,
  "detectionScriptErrorDeviceCount": 1024,
  "detectionScriptPendingDeviceCount": 1024,
  "issueRemediatedDeviceCount": 1024,
  "remediationSkippedDeviceCount": 1024,
  "issueReoccurredDeviceCount": 1024,
  "remediationScriptErrorDeviceCount": 1024,
  "lastScriptRunDateTime": "String (timestamp)",
  "issueRemediatedCumulativeDeviceCount": 1024
}
```




