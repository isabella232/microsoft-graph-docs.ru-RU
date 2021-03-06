---
title: Тип ресурса Девицеманажементаутопилотевент
description: Представляет событие процесса автопилота.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 20fc18da2f6c123b82a9e04d3110313dd830d041
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49258726"
---
# <a name="devicemanagementautopilotevent-resource-type"></a>Тип ресурса Девицеманажементаутопилотевент

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Представляет событие процесса автопилота.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список Девицеманажементаутопилотевентс](../api/intune-troubleshooting-devicemanagementautopilotevent-list.md)|Коллекция [девицеманажементаутопилотевент](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)|Список свойств и связей объектов [девицеманажементаутопилотевент](../resources/intune-troubleshooting-devicemanagementautopilotevent.md) .|
|[Получение Девицеманажементаутопилотевент](../api/intune-troubleshooting-devicemanagementautopilotevent-get.md)|[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)|Чтение свойств и связей объекта [девицеманажементаутопилотевент](../resources/intune-troubleshooting-devicemanagementautopilotevent.md) .|
|[Создание Девицеманажементаутопилотевент](../api/intune-troubleshooting-devicemanagementautopilotevent-create.md)|[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)|Создание нового объекта [девицеманажементаутопилотевент](../resources/intune-troubleshooting-devicemanagementautopilotevent.md) .|
|[Удаление Девицеманажементаутопилотевент](../api/intune-troubleshooting-devicemanagementautopilotevent-delete.md)|Нет|Удаляет объект [девицеманажементаутопилотевент](../resources/intune-troubleshooting-devicemanagementautopilotevent.md).|
|[Обновление Девицеманажементаутопилотевент](../api/intune-troubleshooting-devicemanagementautopilotevent-update.md)|[deviceManagementAutopilotEvent](../resources/intune-troubleshooting-devicemanagementautopilotevent.md)|Обновление свойств объекта [девицеманажементаутопилотевент](../resources/intune-troubleshooting-devicemanagementautopilotevent.md) .|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|UUID объекта.|
|deviceId|String|Идентификатор устройства, связанный с объектом|
|eventDateTime|DateTimeOffset|Время возникновения события.|
|девицерегистереддатетиме|DateTimeOffset|Дата регистрации устройства.|
|енроллментстартдатетиме|DateTimeOffset|Дата начала регистрации устройства.|
|enrollmentType|[windowsAutopilotEnrollmentType](../resources/intune-troubleshooting-windowsautopilotenrollmenttype.md)|Тип регистрации. Возможные значения: `unknown`, `azureADJoinedWithAutopilotProfile`, `offlineDomainJoined`, `azureADJoinedUsingDeviceAuthWithAutopilotProfile`, `azureADJoinedUsingDeviceAuthWithoutAutopilotProfile`, `azureADJoinedWithOfflineAutopilotProfile`, `azureADJoinedWithWhiteGlove`, `offlineDomainJoinedWithWhiteGlove`, `offlineDomainJoinedWithOfflineAutopilotProfile`.|
|девицесериалнумбер|String|Серийный номер устройства.|
|managedDeviceName|String|Управляемое имя устройства.|
|userPrincipalName|String|Имя участника пользователя, используемое для регистрации устройства.|
|виндовсаутопилотдеплойментпрофиледисплайнаме|String|Имя профиля для автопилота.|
|енроллментстате|[енроллментстате](../resources/intune-shared-enrollmentstate.md)|Не удалось зарегистрировать состояние регистрации, например "зарегистрировано". Возможные значения: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.|
|windows10EnrollmentCompletionPageConfigurationDisplayName|String|Имя профиля страницы состояния регистрации|
|деплойментстате|[windowsAutopilotDeploymentState](../resources/intune-troubleshooting-windowsautopilotdeploymentstate.md)|Состояние развертывания, например успешное выполнение, сбой, выполнение, Сукцессвистимеаут. Возможные значения: `unknown`, `success`, `inProgress`, `failure`, `successWithTimeout`.|
|osVersion|String|Версия операционной системы устройства.|
|деплойментдуратион|Длительность|Длительность развертывания с автопилотной версией, включая регистрацию.|
|деплойменттоталдуратион|Длительность|Общее время развертывания с экрана регистрации на рабочем столе.|
|девицепрепаратиондуратион|Длительность|Время, затраченное на регистрацию устройств.|
|девицесетупдуратион|Длительность|Время, затраченное на устройство ESP.|
|аккаунтсетупдуратион|Длительность|Время, затраченное на ESP пользователем.|
|деплойментстартдатетиме|DateTimeOffset|Время начала развертывания.|
|деплойментенддатетиме|DateTimeOffset|Время окончания развертывания.|
|таржетедаппкаунт|Int32|Количество целевых приложений.|
|таржетедполицикаунт|Int32|Количество целевых политик.|
|енроллментфаилуредетаилс|String|Сведения о сбоях при регистрации.|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|полицистатусдетаилс|Коллекция [девицеманажементаутопилотполицистатусдетаил](../resources/intune-troubleshooting-devicemanagementautopilotpolicystatusdetail.md)|Сведения о политике и состоянии приложения для этого устройства.|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementAutopilotEvent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementAutopilotEvent",
  "id": "String (identifier)",
  "deviceId": "String",
  "eventDateTime": "String (timestamp)",
  "deviceRegisteredDateTime": "String (timestamp)",
  "enrollmentStartDateTime": "String (timestamp)",
  "enrollmentType": "String",
  "deviceSerialNumber": "String",
  "managedDeviceName": "String",
  "userPrincipalName": "String",
  "windowsAutopilotDeploymentProfileDisplayName": "String",
  "enrollmentState": "String",
  "windows10EnrollmentCompletionPageConfigurationDisplayName": "String",
  "deploymentState": "String",
  "osVersion": "String",
  "deploymentDuration": "String (duration)",
  "deploymentTotalDuration": "String (duration)",
  "devicePreparationDuration": "String (duration)",
  "deviceSetupDuration": "String (duration)",
  "accountSetupDuration": "String (duration)",
  "deploymentStartDateTime": "String (timestamp)",
  "deploymentEndDateTime": "String (timestamp)",
  "targetedAppCount": 1024,
  "targetedPolicyCount": 1024,
  "enrollmentFailureDetails": "String"
}
```




