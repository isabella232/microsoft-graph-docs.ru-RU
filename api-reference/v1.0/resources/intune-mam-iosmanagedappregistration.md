---
title: Тип ресурса iosManagedAppRegistration
description: Представляет собой сведения о синхронизации управляемого приложения iOS для определенного пользователя. Ресурс ManagedAppRegistration представляет собой сведения об управляемом приложении, используемом членом организации.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: a0896e848cc83bb2671b0a8d4160ec9dace5ca7d
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48088505"
---
# <a name="iosmanagedappregistration-resource-type"></a>Тип ресурса iosManagedAppRegistration

Пространство имен: microsoft.graph

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Представляет собой сведения о синхронизации управляемого приложения iOS для определенного пользователя.
Ресурс ManagedAppRegistration представляет собой сведения об управляемом приложении, используемом членом организации.


Наследуется от [managedAppRegistration](../resources/intune-mam-managedappregistration.md).

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Перечисление iosManagedAppRegistrations](../api/intune-mam-iosmanagedappregistration-list.md)|Коллекция [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md)|Список свойств и связей объектов [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md).|
|[Получение iosManagedAppRegistration](../api/intune-mam-iosmanagedappregistration-get.md)|[iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md)|Чтение свойств и связей объекта [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md).|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|createdDateTime|DateTimeOffset|Дата и время создания. Наследуется от объекта [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|lastSyncDateTime|DateTimeOffset|Дата и время последней синхронизации приложения со службой управления. Наследуется от объекта [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|applicationVersion|String|Версия приложения. Наследуется от объекта [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|managementSdkVersion|String|Версия пакета SDK для управления приложениями. Наследуется от объекта [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|platformVersion|String|Версия операционной системы. Наследуется от объекта [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|deviceType|String|Тип устройства узла. Наследуется от объекта [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|deviceTag|String|Тег, который создан с использованием пакета SDK для управления приложениями и позволяет связать приложения, размещенные на одном устройстве. Мы не гарантируем, что приложения будут связаны во всех состояниях. Наследуется от объекта [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|deviceName|String|Имя устройства узла. Наследуется от объекта [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|flaggedReasons|Коллекция [манажедаппфлагжедреасон](../resources/intune-mam-managedappflaggedreason.md)|Нуль или более причин, по которым помечается регистрация приложения Пример: приложение запускается на рутованном устройстве. Наследуется от [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|userId|String|Идентификатор пользователя, к которому относится эта регистрация приложения. Наследуется от объекта [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|appIdentifier|[mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)|Идентификатор пакета приложения. Наследуется от объекта [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|id|Строка|Ключ объекта. Наследуется от объекта [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|version|String|Версия объекта. Наследуется от [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|appliedPolicies|Коллекция объектов [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|Нуль или более политик, примененных к зарегистрированному приложению, когда оно в последний раз синхронизировалось со службой управления. Наследуется от [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|intendedPolicies|Коллекция объектов [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|Нуль или более политик, которые на текущий момент администратор использует для приложения. Наследуется от [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|
|operations|Коллекция объектов [managedAppOperation](../resources/intune-mam-managedappoperation.md)|Нуль или более долговременных операций, запускаемых для регистрации приложения. Наследуется от [managedAppRegistration](../resources/intune-mam-managedappregistration.md).|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosManagedAppRegistration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosManagedAppRegistration",
  "createdDateTime": "String (timestamp)",
  "lastSyncDateTime": "String (timestamp)",
  "applicationVersion": "String",
  "managementSdkVersion": "String",
  "platformVersion": "String",
  "deviceType": "String",
  "deviceTag": "String",
  "deviceName": "String",
  "flaggedReasons": [
    "String"
  ],
  "userId": "String",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier",
    "bundleId": "String"
  },
  "id": "String (identifier)",
  "version": "String"
}
```


<!-- {
  "type": "#page.annotation",
  "suppressions": [
     "Warning: /api-reference/v1.0/resources/intune-mam-iosmanagedappregistration.md/microsoft.graph.iosManagedAppRegistration/flaggedReasons:
    Inconsistent types between parameter (String) and table (Object)"
  ],
}
-->







