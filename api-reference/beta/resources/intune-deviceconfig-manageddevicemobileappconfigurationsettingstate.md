---
title: Тип ресурса Манажеддевицемобилеаппконфигуратионсеттингстате
description: Состояние параметров конфигурации мобильных приложений для управляемых устройств для данного устройства.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: d9e74a4fb9b6739d5051e37af4c15c48ede6bda1
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49302840"
---
# <a name="manageddevicemobileappconfigurationsettingstate-resource-type"></a>Тип ресурса Манажеддевицемобилеаппконфигуратионсеттингстате

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Состояние параметров конфигурации мобильных приложений для управляемых устройств для данного устройства.

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|setting|String|Параметр для отчета|
|settingName|String|Локализованное или понятное имя параметра для отчета|
|instanceDisplayName|String|Имя экземпляра параметра для отчета|
|state|[комплианцестатус](../resources/intune-shared-compliancestatus.md)|Состояние соответствия для параметра. Возможные значения: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.|
|errorCode|Int64|Код ошибки для параметра|
|errorDescription|String|Описание ошибки|
|userId|String|ИД пользователя|
|userName|String|Имя пользователя|
|userEmail|String|Электронный адрес пользователя|
|userPrincipalName|String|Имя участника-пользователя.|
|sources|Коллекция [settingSource](../resources/intune-deviceconfig-settingsource.md)|Соответствующие политики|
|currentValue|String|Текущее значение параметра на устройстве|
|сеттингинстанцеид|String|сеттингинстанцеид|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfigurationSettingState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationSettingState",
  "setting": "String",
  "settingName": "String",
  "instanceDisplayName": "String",
  "state": "String",
  "errorCode": 1024,
  "errorDescription": "String",
  "userId": "String",
  "userName": "String",
  "userEmail": "String",
  "userPrincipalName": "String",
  "sources": [
    {
      "@odata.type": "microsoft.graph.settingSource",
      "id": "String",
      "displayName": "String",
      "sourceType": "String"
    }
  ],
  "currentValue": "String",
  "settingInstanceId": "String"
}
```




