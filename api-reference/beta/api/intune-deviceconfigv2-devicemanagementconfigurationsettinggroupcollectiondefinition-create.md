---
title: Создание Девицеманажементконфигуратионсеттингграупколлектиондефинитион
description: Создание нового объекта Девицеманажементконфигуратионсеттингграупколлектиондефинитион.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: 863a4e9573cf83afb1f2b91334cc771c0036c383
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49242542"
---
# <a name="create-devicemanagementconfigurationsettinggroupcollectiondefinition"></a>Создание Девицеманажементконфигуратионсеттингграупколлектиондефинитион

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Создание нового объекта [девицеманажементконфигуратионсеттингграупколлектиондефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettinggroupcollectiondefinition.md) .

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
POST /deviceManagement/configurationSettings
POST /deviceManagement/configurationPolicies/{deviceManagementConfigurationPolicyId}/settings/{deviceManagementConfigurationSettingId}/settingDefinitions
```

## <a name="request-headers"></a>Заголовки запроса
|Заголовок|Значение|
|:---|:---|
|Авторизация|Bearer &lt;token&gt;. Обязательный.|
|Accept|application/json|

## <a name="request-body"></a>Текст запроса
В тексте запроса добавьте представление объекта Девицеманажементконфигуратионсеттингграупколлектиондефинитион в формате JSON.

В следующей таблице приведены свойства, необходимые при создании Девицеманажементконфигуратионсеттингграупколлектиондефинитион.

|Свойство|Тип|Описание|
|:---|:---|:---|
|применения|[девицеманажементконфигуратионсеттингаппликабилити](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingapplicability.md)|Сведения о том, какие параметры устройства применяются в унаследованном от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|акцесстипес|[девицеманажементконфигуратионсеттингакцесстипес](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingaccesstypes.md)|Режим доступа для чтения и записи параметра, унаследованного от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md). Возможные значения: `none`, `add`, `copy`, `delete`, `get`, `replace`, `execute`.|
|keywords|Коллекция строк|Маркеры, для которых параметры поиска унаследованы от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|инфаурлс|Коллекция строк|Список ссылок дополнительные сведения для параметра можно найти в разделе унаследовано от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|экземпляр|[девицеманажементконфигуратионсеттингоккурренце](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingoccurrence.md)|Указывает, является ли параметр обязательным или не наследуется от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|baseUri|String|Базовый путь поставщика CSP наследуется от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|оффсетури|String|Путь к поставщику службы шифрования из базового наследуемого от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|рутдефинитионид|String|Определение корневого параметра, если параметр является дочерним. Наследуется от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|categoryId|String|Указывает группу областей, в которой параметр настроен в указанном поставщике службы конфигурации (CSP), унаследованном от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|сеттингусаже|[девицеманажементконфигуратионсеттингусаже](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingusage.md)|Тип параметра, например конфигурация и соответствие, наследуемые от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md). Возможные значения: `none`, `configuration`.|
|id|String|Идентификатор элемента, наследуемого из [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|description|String|Описание элемента, наследуемого из [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|helpText|String|Текст справки элемента, наследуемого от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|name|String|Имя элемента, наследуемого из [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|displayName|String|Отображаемое имя элемента, наследуемого от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|version|String|Версия элемента наследуется от [девицеманажементконфигуратионсеттингдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdefinition.md)|
|чилдидс|Коллекция строк|Зависимые параметры дочерних элементов для этой группы параметров, унаследованных от [девицеманажементконфигуратионсеттингграупдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettinggroupdefinition.md)|
|депендентон|Коллекция [девицеманажементконфигуратиондепендентон](../resources/intune-deviceconfigv2-devicemanagementconfigurationdependenton.md)|Список зависимостей для группы параметров, наследуемой от [девицеманажементконфигуратионсеттингграупдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettinggroupdefinition.md)|
|депендедонби|Коллекция [девицеманажементконфигуратионсеттингдепендедонби](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettingdependedonby.md)|Список дочерних параметров, зависящих от этого параметра, наследуемого от [девицеманажементконфигуратионсеттингграупдефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettinggroupdefinition.md)|
|максимумкаунт|Int32|Максимальное число параметров для параметра количество групп в коллекции. Допустимые значения — от 1 до 100|
|минимумкаунт|Int32|Минимальное число параметров в коллекции. Допустимые значения — от 1 до 100|



## <a name="response"></a>Отклик
В случае успешного выполнения этот метод возвращает `201 Created` код отклика и объект [девицеманажементконфигуратионсеттингграупколлектиондефинитион](../resources/intune-deviceconfigv2-devicemanagementconfigurationsettinggroupcollectiondefinition.md) в тексте отклика.

## <a name="example"></a>Пример

### <a name="request"></a>Запрос
Ниже приведен пример запроса.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/configurationSettings
Content-type: application/json
Content-length: 1504

{
  "@odata.type": "#microsoft.graph.deviceManagementConfigurationSettingGroupCollectionDefinition",
  "applicability": {
    "@odata.type": "microsoft.graph.deviceManagementConfigurationSettingApplicability",
    "description": "Description value",
    "platform": "macOS",
    "deviceMode": "kiosk",
    "technologies": "mdm"
  },
  "accessTypes": "add",
  "keywords": [
    "Keywords value"
  ],
  "infoUrls": [
    "Info Urls value"
  ],
  "occurrence": {
    "@odata.type": "microsoft.graph.deviceManagementConfigurationSettingOccurrence",
    "minDeviceOccurrence": 3,
    "maxDeviceOccurrence": 3
  },
  "baseUri": "Base Uri value",
  "offsetUri": "Offset Uri value",
  "rootDefinitionId": "Root Definition Id value",
  "categoryId": "Category Id value",
  "settingUsage": "configuration",
  "description": "Description value",
  "helpText": "Help Text value",
  "name": "Name value",
  "displayName": "Display Name value",
  "version": "Version value",
  "childIds": [
    "Child Ids value"
  ],
  "dependentOn": [
    {
      "@odata.type": "microsoft.graph.deviceManagementConfigurationDependentOn",
      "dependentOn": "Dependent On value",
      "parentSettingId": "Parent Setting Id value"
    }
  ],
  "dependedOnBy": [
    {
      "@odata.type": "microsoft.graph.deviceManagementConfigurationSettingDependedOnBy",
      "dependedOnBy": "Depended On By value",
      "required": true
    }
  ],
  "maximumCount": 12,
  "minimumCount": 12
}
```

### <a name="response"></a>Отклик
Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1553

{
  "@odata.type": "#microsoft.graph.deviceManagementConfigurationSettingGroupCollectionDefinition",
  "applicability": {
    "@odata.type": "microsoft.graph.deviceManagementConfigurationSettingApplicability",
    "description": "Description value",
    "platform": "macOS",
    "deviceMode": "kiosk",
    "technologies": "mdm"
  },
  "accessTypes": "add",
  "keywords": [
    "Keywords value"
  ],
  "infoUrls": [
    "Info Urls value"
  ],
  "occurrence": {
    "@odata.type": "microsoft.graph.deviceManagementConfigurationSettingOccurrence",
    "minDeviceOccurrence": 3,
    "maxDeviceOccurrence": 3
  },
  "baseUri": "Base Uri value",
  "offsetUri": "Offset Uri value",
  "rootDefinitionId": "Root Definition Id value",
  "categoryId": "Category Id value",
  "settingUsage": "configuration",
  "id": "739da194-a194-739d-94a1-9d7394a19d73",
  "description": "Description value",
  "helpText": "Help Text value",
  "name": "Name value",
  "displayName": "Display Name value",
  "version": "Version value",
  "childIds": [
    "Child Ids value"
  ],
  "dependentOn": [
    {
      "@odata.type": "microsoft.graph.deviceManagementConfigurationDependentOn",
      "dependentOn": "Dependent On value",
      "parentSettingId": "Parent Setting Id value"
    }
  ],
  "dependedOnBy": [
    {
      "@odata.type": "microsoft.graph.deviceManagementConfigurationSettingDependedOnBy",
      "dependedOnBy": "Depended On By value",
      "required": true
    }
  ],
  "maximumCount": 12,
  "minimumCount": 12
}
```




