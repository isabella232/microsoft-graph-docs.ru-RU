---
title: Тип ресурса networkIPv6ConfigurationManagementCondition
description: Можно определить условия управления на основе конфигурации IPv6, которые будут вызываться, когда устройство обнаружит определенные параметры IP-сети. Условие управления IP-конфигурацией считается ИСТИНным, только если сетевое подключение активно. Адреса DHCP-серверов IPv6 могут быть несогласованными. Это связано с тем, что Windows (цирка Редстоне) не предоставляет эту информацию в службу естественной проверки подлинности.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: c6230478ec44698c3897b726c49043a48f078b02
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49299081"
---
# <a name="networkipv6configurationmanagementcondition-resource-type"></a>Тип ресурса networkIPv6ConfigurationManagementCondition

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Можно определить условия управления на основе конфигурации IPv6, которые будут вызываться, когда устройство обнаружит определенные параметры IP-сети. Условие управления IP-конфигурацией считается ИСТИНным, только если сетевое подключение активно.
Адреса DHCP-серверов IPv6 могут быть несогласованными. Это связано с тем, что Windows (цирка Редстоне) не предоставляет эту информацию в службу естественной проверки подлинности.


Наследуется от [нетворкманажементкондитион](../resources/intune-fencing-networkmanagementcondition.md)

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список networkIPv6ConfigurationManagementConditions](../api/intune-fencing-networkipv6configurationmanagementcondition-list.md)|Коллекция [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md)|Список свойств и связей объектов [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) .|
|[Получение networkIPv6ConfigurationManagementCondition](../api/intune-fencing-networkipv6configurationmanagementcondition-get.md)|[networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md)|Чтение свойств и связей объекта [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) .|
|[Создание networkIPv6ConfigurationManagementCondition](../api/intune-fencing-networkipv6configurationmanagementcondition-create.md)|[networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md)|Создание нового объекта [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) .|
|[Удаление networkIPv6ConfigurationManagementCondition](../api/intune-fencing-networkipv6configurationmanagementcondition-delete.md)|Нет|Удаляет объект [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md).|
|[Обновление networkIPv6ConfigurationManagementCondition](../api/intune-fencing-networkipv6configurationmanagementcondition-update.md)|[networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md)|Обновление свойств объекта [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) .|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Уникальный идентификатор для условия управления. Созданное системой значение, назначаемое при создании. Наследуется от [манажементкондитион](../resources/intune-fencing-managementcondition.md)|
|uniqueName|String|Уникальное имя условия управления. Используется в выражениях условия управления. Наследуется от [манажементкондитион](../resources/intune-fencing-managementcondition.md)|
|displayName|String|Имя условия управления, определенное администратором. Наследуется от [манажементкондитион](../resources/intune-fencing-managementcondition.md)|
|description|String|Описание условия управления, заданное администратором. Наследуется от [манажементкондитион](../resources/intune-fencing-managementcondition.md)|
|createdDateTime|DateTimeOffset|Время создания условия управления. Созданная сторона службы. Наследуется от [манажементкондитион](../resources/intune-fencing-managementcondition.md)|
|modifiedDateTime|DateTimeOffset|Время последнего изменения условия управления. Обновленная сторона службы. Наследуется от [манажементкондитион](../resources/intune-fencing-managementcondition.md)|
|eTag|String|Тег ETag условия управления. Обновленная сторона службы. Наследуется от [манажементкондитион](../resources/intune-fencing-managementcondition.md)|
|аппликаблеплатформс|Коллекция [девицеплатформтипе](../resources/intune-shared-deviceplatformtype.md)|Соответствующие платформы для этого условия управления. Наследуется от [манажементкондитион](../resources/intune-fencing-managementcondition.md)|
|ipV6Prefix|String|Подсеть IPv6, к которой необходимо подключиться. Например: 2001: db8::/32|
|ipV6Gateway|String|Адрес шлюза IPv6 в. Например, 2001: db8:: 1|
|ipV6DNSServerList|Коллекция строк|DNS-серверы IPv6, настроенные для адаптера.|
|днссуффикслист|Коллекция строк|Допустимые DNS-суффиксы для текущей сети. Например, seattle.contoso.com|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|манажементкондитионстатементс|Коллекция [манажементкондитионстатемент](../resources/intune-fencing-managementconditionstatement.md)|Операторы условия управления, связанные с условием управления. Наследуется от [манажементкондитион](../resources/intune-fencing-managementcondition.md)|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.networkIPv6ConfigurationManagementCondition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.networkIPv6ConfigurationManagementCondition",
  "id": "String (identifier)",
  "uniqueName": "String",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "eTag": "String",
  "applicablePlatforms": [
    "String"
  ],
  "ipV6Prefix": "String",
  "ipV6Gateway": "String",
  "ipV6DNSServerList": [
    "String"
  ],
  "dnsSuffixList": [
    "String"
  ]
}
```




