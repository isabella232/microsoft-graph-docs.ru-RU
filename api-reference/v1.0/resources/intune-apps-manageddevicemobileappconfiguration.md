---
title: Тип ресурса managedDeviceMobileAppConfiguration
description: Абстрактный класс для настройки мобильного приложения для зарегистрированных устройств.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 4a8954b276ce297f3a304a0a408ec22063ee3634
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48015425"
---
# <a name="manageddevicemobileappconfiguration-resource-type"></a>Тип ресурса managedDeviceMobileAppConfiguration

Пространство имен: microsoft.graph

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Абстрактный класс для настройки мобильного приложения для зарегистрированных устройств.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список managedDeviceMobileAppConfigurations](../api/intune-apps-manageddevicemobileappconfiguration-list.md)|Коллекция [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)|Перечисление свойств и связей объектов [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).|
|[Получение объекта managedDeviceMobileAppConfiguration](../api/intune-apps-manageddevicemobileappconfiguration-get.md)|[managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)|Чтение свойств и связей объекта [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).|
|[Действие assign](../api/intune-apps-manageddevicemobileappconfiguration-assign.md)|Нет|Н/Д|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Ключ объекта.|
|targetedMobileApps|Коллекция String|Связанное приложение.|
|createdDateTime|DateTimeOffset|Дата и время создания объекта.|
|description|String|Указанное администратором описание конфигурации устройства.|
|lastModifiedDateTime|DateTimeOffset|Дата и время последнего изменения объекта.|
|displayName|String|Указанное администратором имя конфигурации устройства.|
|version|Int32|Версия конфигурации устройства.|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|assignments|Коллекция [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md)|Список заданий группы для настройки приложения.|
|deviceStatuses|Коллекция [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md)|Список ManagedDeviceMobileAppConfigurationDeviceStatus.|
|userStatuses|Коллекция [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md)|Список объектов ManagedDeviceMobileAppConfigurationUserStatus.|
|deviceStatusSummary|[managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md)|Общие сведения о состоянии устройства, связанном с настройкой приложения.|
|userStatusSummary|[managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|Общие сведения о состоянии пользователя, связанном с настройкой приложения.|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfiguration",
  "id": "String (identifier)",
  "targetedMobileApps": [
    "String"
  ],
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024
}
```









