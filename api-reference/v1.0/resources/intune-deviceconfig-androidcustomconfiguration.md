---
title: Тип ресурса androidCustomConfiguration
description: В этой статье описаны объявляемые методы, свойства и связи, которые предоставляются ресурсом androidCustomConfiguration.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 7674400d6d0ec364ebc4866fb1f2445ae98612e4
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48041577"
---
# <a name="androidcustomconfiguration-resource-type"></a>Тип ресурса androidCustomConfiguration

Пространство имен: microsoft.graph

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

В этой статье описаны объявляемые методы, свойства и связи, которые предоставляются ресурсом androidCustomConfiguration.


Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Перечисление androidCustomConfigurations](../api/intune-deviceconfig-androidcustomconfiguration-list.md)|Коллекция [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md)|Перечисление свойств и связей объектов [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md).|
|[Получение androidCustomConfiguration](../api/intune-deviceconfig-androidcustomconfiguration-get.md)|[androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md)|Считывание свойств и связей объекта [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md).|
|[Создание androidCustomConfiguration](../api/intune-deviceconfig-androidcustomconfiguration-create.md)|[androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md)|Создание объекта [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md).|
|[Удаление androidCustomConfiguration](../api/intune-deviceconfig-androidcustomconfiguration-delete.md)|None|Удаление экземпляра [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md).|
|[Обновление androidCustomConfiguration](../api/intune-deviceconfig-androidcustomconfiguration-update.md)|[androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md)|Обновление свойств объекта [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md).|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Ключ объекта. Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|lastModifiedDateTime|DateTimeOffset|Дата и время последнего изменения объекта. Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|createdDateTime|DateTimeOffset|Дата и время создания объекта. Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|description|String|Указанное администратором описание конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|displayName|String|Указанное администратором имя конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|version|Int32|Версия конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|omaSettings|Коллекция [omaSetting](../resources/intune-deviceconfig-omasetting.md)|Параметры OMA. Эта коллекция может содержать не более 1000 элементов.|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|assignments|Коллекция [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|Список назначений для профиля конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|deviceStatuses|Коллекция [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Состояние установки конфигурации для каждого устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|userStatuses|Коллекция [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|Состояние установки конфигурации устройств пользователем. Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|Обзор состояния конфигурации устройств. Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|Обзор состояния конфигурации устройств для пользователей. Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|deviceSettingStateSummaries|Коллекция [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Сводка данных о состоянии настройки конфигурации устройств. Наследуется от [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidCustomConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidCustomConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSetting",
      "displayName": "String",
      "description": "String",
      "omaUri": "String",
      "value": 1024
    }
  ]
}
```









