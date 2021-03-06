---
title: Тип ресурса Девицеманажементтемплате
description: Объект, представляющий определенную коллекцию параметров устройства
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 9f6d30b8b752c030a0b94c9269ab22a143f5857e
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49209509"
---
# <a name="devicemanagementtemplate-resource-type"></a>Тип ресурса Девицеманажементтемплате

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Объект, представляющий определенную коллекцию параметров устройства

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список Девицеманажементтемплатес](../api/intune-deviceintent-devicemanagementtemplate-list.md)|Коллекция [девицеманажементтемплате](../resources/intune-deviceintent-devicemanagementtemplate.md)|Список свойств и связей объектов [девицеманажементтемплате](../resources/intune-deviceintent-devicemanagementtemplate.md) .|
|[Получение Девицеманажементтемплате](../api/intune-deviceintent-devicemanagementtemplate-get.md)|[deviceManagementTemplate](../resources/intune-deviceintent-devicemanagementtemplate.md)|Чтение свойств и связей объекта [девицеманажементтемплате](../resources/intune-deviceintent-devicemanagementtemplate.md) .|
|[Создание Девицеманажементтемплате](../api/intune-deviceintent-devicemanagementtemplate-create.md)|[deviceManagementTemplate](../resources/intune-deviceintent-devicemanagementtemplate.md)|Создание нового объекта [девицеманажементтемплате](../resources/intune-deviceintent-devicemanagementtemplate.md) .|
|[Удаление Девицеманажементтемплате](../api/intune-deviceintent-devicemanagementtemplate-delete.md)|Нет|Удаляет объект [девицеманажементтемплате](../resources/intune-deviceintent-devicemanagementtemplate.md).|
|[Обновление Девицеманажементтемплате](../api/intune-deviceintent-devicemanagementtemplate-update.md)|[deviceManagementTemplate](../resources/intune-deviceintent-devicemanagementtemplate.md)|Обновление свойств объекта [девицеманажементтемплате](../resources/intune-deviceintent-devicemanagementtemplate.md) .|
|[Действие createInstance](../api/intune-deviceintent-devicemanagementtemplate-createinstance.md)|[deviceManagementIntent](../resources/intune-deviceintent-devicemanagementintent.md)|Пока не задокументировано.|
|[Функция Compare](../api/intune-deviceintent-devicemanagementtemplate-compare.md)|Коллекция [девицеманажементсеттингкомпарисон](../resources/intune-deviceintent-devicemanagementsettingcomparison.md)|Пока не задокументировано.|
|[действие importOffice365DeviceConfigurationPolicies](../api/intune-deviceintent-devicemanagementtemplate-importoffice365deviceconfigurationpolicies.md)|Коллекция [девицеманажементинтент](../resources/intune-deviceintent-devicemanagementintent.md)|Н/Д|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Идентификатор шаблона|
|displayName|String|Отображаемое имя шаблона|
|description|String|Описание шаблона|
|versionInfo|String|Сведения о версии шаблона|
|нерекомендуемый|Boolean|Шаблон устарел или не является устаревшим. Не удается создать объект "удержания" из устаревшего шаблона.|
|интенткаунт|Int32|Количество целей, созданных на основе этого шаблона.|
|TemplateType — тип|[deviceManagementTemplateType](../resources/intune-deviceintent-devicemanagementtemplatetype.md)|Тип шаблона. Возможные значения: `securityBaseline`, `specializedDevices`, `advancedThreatProtectionSecurityBaseline`, `deviceConfiguration`, `custom`, `securityTemplate`, `microsoftEdgeSecurityBaseline`, `microsoftOffice365ProPlusSecurityBaseline`, `deviceCompliance`, `deviceConfigurationForOffice365`, `cloudPC`, `firewallSharedSettings`.|
|platformType|[полициплатформтипе](../resources/intune-shared-policyplatformtype.md)|Платформа шаблона. Возможные значения: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`, `windows10XProfile`, `all`.|
|темплатесубтипе|[deviceManagementTemplateSubtype](../resources/intune-deviceintent-devicemanagementtemplatesubtype.md)|Подтип шаблона. Возможные значения: `none`, `firewall`, `diskEncryption`, `attackSurfaceReduction`, `endpointDetectionReponse`, `accountProtection`, `antivirus`, `firewallSharedAppList`, `firewallSharedIpList`, `firewallSharedPortlist`.|
|publishedDateTime|DateTimeOffset|При публикации шаблона|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|параметры|Коллекция [девицеманажементсеттингинстанце](../resources/intune-deviceintent-devicemanagementsettinginstance.md)|Коллекция всех параметров, которые содержит этот шаблон|
|categories|Коллекция [девицеманажементтемплатесеттингкатегори](../resources/intune-deviceintent-devicemanagementtemplatesettingcategory.md)|Коллекция настроек категорий в шаблоне|
|мигратаблето|Коллекция [девицеманажементтемплате](../resources/intune-deviceintent-devicemanagementtemplate.md)|Коллекция шаблонов, в которые можно перенести этот шаблон|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementTemplate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementTemplate",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "versionInfo": "String",
  "isDeprecated": true,
  "intentCount": 1024,
  "templateType": "String",
  "platformType": "String",
  "templateSubtype": "String",
  "publishedDateTime": "String (timestamp)"
}
```




