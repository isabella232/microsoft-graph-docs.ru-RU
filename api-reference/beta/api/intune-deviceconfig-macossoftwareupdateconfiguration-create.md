---
title: Создание Макоссофтвареупдатеконфигуратион
description: Создание нового объекта Макоссофтвареупдатеконфигуратион.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: 1ccfe7f0dc7fc8f25899bcc3afba09f81993daa2
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49236444"
---
# <a name="create-macossoftwareupdateconfiguration"></a>Создание Макоссофтвареупдатеконфигуратион

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Создание нового объекта [макоссофтвареупдатеконфигуратион](../resources/intune-deviceconfig-macossoftwareupdateconfiguration.md) .

## <a name="prerequisites"></a>Необходимые компоненты
Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

|Тип разрешения|Разрешения (в порядке убывания привилегий)|
|:---|:---|
|Делегированные (рабочая или учебная учетная запись)|DeviceManagementConfiguration.ReadWrite.All|
|Делегированные (личная учетная запись Майкрософт)|Не поддерживается.|
|Приложение|DeviceManagementConfiguration.ReadWrite.All|

## <a name="http-request"></a>HTTP-запрос
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a>Заголовки запроса
|Заголовок|Значение|
|:---|:---|
|Авторизация|Bearer &lt;token&gt;. Обязательный.|
|Accept|application/json|

## <a name="request-body"></a>Текст запроса
В тексте запроса добавьте представление объекта Макоссофтвареупдатеконфигуратион в формате JSON.

В следующей таблице приведены свойства, необходимые при создании Макоссофтвареупдатеконфигуратион.

|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Ключ объекта. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|lastModifiedDateTime|DateTimeOffset|Дата и время последнего изменения объекта. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|roleScopeTagIds|Коллекция строк|Список тегов областей для этого экземпляра сущности. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|суппортсскопетагс|Boolean|Указывает, поддерживает ли базовая конфигурация устройства назначение тегов области. Назначение свойства Скопетагс не разрешено, если это значение равно false, а сущности не будут отображаться для пользователей с ограниченной областью действия. Это происходит для устаревших политик, созданных в Silverlight, и может быть разрешено путем удаления и повторного создания политики на портале Azure. Это свойство доступно только для чтения. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|deviceManagementApplicabilityRuleOsEdition|[deviceManagementApplicabilityRuleOsEdition](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosedition.md)|Применимость выпусков ОС для этой политики. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|deviceManagementApplicabilityRuleOsVersion|[deviceManagementApplicabilityRuleOsVersion](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosversion.md)|Правило применимости версии ОС для этой политики. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|deviceManagementApplicabilityRuleDeviceMode|[deviceManagementApplicabilityRuleDeviceMode](../resources/intune-deviceconfig-devicemanagementapplicabilityruledevicemode.md)|Правило применимости режима устройства для этой политики. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|createdDateTime|DateTimeOffset|Дата и время создания объекта. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|description|String|Указанное администратором описание конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|displayName|String|Указанное администратором имя конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|version|Int32|Версия конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|критикалупдатебехавиор|[macOSSoftwareUpdateBehavior](../resources/intune-deviceconfig-macossoftwareupdatebehavior.md)|Обновление поведения критических обновлений. Возможные значения: `notConfigured`, `default`.|
|конфигдатаупдатебехавиор|[macOSSoftwareUpdateBehavior](../resources/intune-deviceconfig-macossoftwareupdatebehavior.md)|Обновление поведения обновлений файлов данных конфигурации. Возможные значения: `notConfigured`, `default`.|
|фирмвареупдатебехавиор|[macOSSoftwareUpdateBehavior](../resources/intune-deviceconfig-macossoftwareupdatebehavior.md)|Обновление поведения обновлений микропрограммного обеспечения. Возможные значения: `notConfigured`, `default`.|
|аллосерупдатебехавиор|[macOSSoftwareUpdateBehavior](../resources/intune-deviceconfig-macossoftwareupdatebehavior.md)|Обновление поведения для всех остальных обновлений. Возможные значения: `notConfigured`, `default`.|
|упдатесчедулетипе|[macOSSoftwareUpdateScheduleType](../resources/intune-deviceconfig-macossoftwareupdatescheduletype.md)|Обновление типа расписания. Возможные значения: `alwaysUpdate`, `updateDuringTimeWindows`, `updateOutsideOfTimeWindows`.|
|кустомупдатетимевиндовс|Коллекция [кустомупдатетимевиндов](../resources/intune-deviceconfig-customupdatetimewindow.md)|Настраиваемое время Windows, когда обновления будут разрешены или заблокированы. Эта коллекция может содержать не более 20 элементов.|
|упдатетимевиндовуткоффсетинминутес|Int32|Минуты, указывающие смещение UTC для каждого периода обновления|



## <a name="response"></a>Отклик
В случае успешного выполнения этот метод возвращает `201 Created` код отклика и объект [макоссофтвареупдатеконфигуратион](../resources/intune-deviceconfig-macossoftwareupdateconfiguration.md) в тексте отклика.

## <a name="example"></a>Пример

### <a name="request"></a>Запрос
Ниже приведен пример запроса.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1542

{
  "@odata.type": "#microsoft.graph.macOSSoftwareUpdateConfiguration",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "deviceManagementApplicabilityRuleOsEdition": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsEdition",
    "osEditionTypes": [
      "windows10EnterpriseN"
    ],
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleOsVersion": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsVersion",
    "minOSVersion": "Min OSVersion value",
    "maxOSVersion": "Max OSVersion value",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleDeviceMode": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleDeviceMode",
    "deviceMode": "sModeConfiguration",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "criticalUpdateBehavior": "default",
  "configDataUpdateBehavior": "default",
  "firmwareUpdateBehavior": "default",
  "allOtherUpdateBehavior": "default",
  "updateScheduleType": "updateDuringTimeWindows",
  "customUpdateTimeWindows": [
    {
      "@odata.type": "microsoft.graph.customUpdateTimeWindow",
      "startDay": "monday",
      "endDay": "monday",
      "startTime": "12:03:30.2730000",
      "endTime": "12:03:02.3740000"
    }
  ],
  "updateTimeWindowUtcOffsetInMinutes": 2
}
```

### <a name="response"></a>Отклик
Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1714

{
  "@odata.type": "#microsoft.graph.macOSSoftwareUpdateConfiguration",
  "id": "b8e467ac-67ac-b8e4-ac67-e4b8ac67e4b8",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "deviceManagementApplicabilityRuleOsEdition": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsEdition",
    "osEditionTypes": [
      "windows10EnterpriseN"
    ],
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleOsVersion": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsVersion",
    "minOSVersion": "Min OSVersion value",
    "maxOSVersion": "Max OSVersion value",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleDeviceMode": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleDeviceMode",
    "deviceMode": "sModeConfiguration",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "criticalUpdateBehavior": "default",
  "configDataUpdateBehavior": "default",
  "firmwareUpdateBehavior": "default",
  "allOtherUpdateBehavior": "default",
  "updateScheduleType": "updateDuringTimeWindows",
  "customUpdateTimeWindows": [
    {
      "@odata.type": "microsoft.graph.customUpdateTimeWindow",
      "startDay": "monday",
      "endDay": "monday",
      "startTime": "12:03:30.2730000",
      "endTime": "12:03:02.3740000"
    }
  ],
  "updateTimeWindowUtcOffsetInMinutes": 2
}
```




