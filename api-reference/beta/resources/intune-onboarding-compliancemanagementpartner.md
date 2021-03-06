---
title: Тип ресурса Комплианцеманажементпартнер
description: Партнер по управлению соответствием для всех платформ
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 328b0df7f956488756558d6838fd501fac28d1c9
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49222753"
---
# <a name="compliancemanagementpartner-resource-type"></a>Тип ресурса Комплианцеманажементпартнер

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Партнер по управлению соответствием для всех платформ

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список Комплианцеманажементпартнерс](../api/intune-onboarding-compliancemanagementpartner-list.md)|Коллекция [комплианцеманажементпартнер](../resources/intune-onboarding-compliancemanagementpartner.md)|Список свойств и связей объектов [комплианцеманажементпартнер](../resources/intune-onboarding-compliancemanagementpartner.md) .|
|[Получение Комплианцеманажементпартнер](../api/intune-onboarding-compliancemanagementpartner-get.md)|[complianceManagementPartner](../resources/intune-onboarding-compliancemanagementpartner.md)|Чтение свойств и связей объекта [комплианцеманажементпартнер](../resources/intune-onboarding-compliancemanagementpartner.md) .|
|[Создание Комплианцеманажементпартнер](../api/intune-onboarding-compliancemanagementpartner-create.md)|[complianceManagementPartner](../resources/intune-onboarding-compliancemanagementpartner.md)|Создание нового объекта [комплианцеманажементпартнер](../resources/intune-onboarding-compliancemanagementpartner.md) .|
|[Удаление Комплианцеманажементпартнер](../api/intune-onboarding-compliancemanagementpartner-delete.md)|Нет|Удаляет объект [комплианцеманажементпартнер](../resources/intune-onboarding-compliancemanagementpartner.md).|
|[Обновление Комплианцеманажементпартнер](../api/intune-onboarding-compliancemanagementpartner-update.md)|[complianceManagementPartner](../resources/intune-onboarding-compliancemanagementpartner.md)|Обновление свойств объекта [комплианцеманажементпартнер](../resources/intune-onboarding-compliancemanagementpartner.md) .|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Идентификатор объекта|
|lastHeartbeatDateTime|DateTimeOffset|Метка времени последнего пакета пульса после того, как администратор направил соответствие партнеру управления соответствием|
|partnerState|[девицеманажементпартнертенантстате](../resources/intune-onboarding-devicemanagementpartnertenantstate.md)|Состояние партнера этого клиента. Возможные значения: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.|
|displayName|String|Отображаемое имя партнера|
|макосонбоардед|Boolean|Партнер, подключенный к устройствам Mac.|
|виндовсонбоардед|Boolean|Партнер, направленный на устройства с Windows.|
|андроидонбоардед|Boolean|Партнер, направленный на устройства с Android.|
|иосонбоардед|Boolean|Партнер, подключенный к устройствам iOS.|
|макосенроллментассигнментс|Коллекция [комплианцеманажементпартнерассигнмент](../resources/intune-onboarding-compliancemanagementpartnerassignment.md)|Группы пользователей, которые регистрируют устройства Mac через партнера.|
|виндовсенроллментассигнментс|Коллекция [комплианцеманажементпартнерассигнмент](../resources/intune-onboarding-compliancemanagementpartnerassignment.md)|Группы пользователей, которые регистрируют устройства Windows с помощью партнера.|
|андроиденроллментассигнментс|Коллекция [комплианцеманажементпартнерассигнмент](../resources/intune-onboarding-compliancemanagementpartnerassignment.md)|Группы пользователей, которые регистрируют устройства с Android через партнера.|
|иосенроллментассигнментс|Коллекция [комплианцеманажементпартнерассигнмент](../resources/intune-onboarding-compliancemanagementpartnerassignment.md)|Группы пользователей, которые регистрируют устройства с iOS через партнера.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.complianceManagementPartner"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.complianceManagementPartner",
  "id": "String (identifier)",
  "lastHeartbeatDateTime": "String (timestamp)",
  "partnerState": "String",
  "displayName": "String",
  "macOsOnboarded": true,
  "windowsOnboarded": true,
  "androidOnboarded": true,
  "iosOnboarded": true,
  "macOsEnrollmentAssignments": [
    {
      "@odata.type": "microsoft.graph.complianceManagementPartnerAssignment",
      "target": {
        "@odata.type": "microsoft.graph.allDevicesAssignmentTarget",
        "deviceAndAppManagementAssignmentFilterId": "String",
        "deviceAndAppManagementAssignmentFilterType": "String"
      }
    }
  ],
  "windowsEnrollmentAssignments": [
    {
      "@odata.type": "microsoft.graph.complianceManagementPartnerAssignment",
      "target": {
        "@odata.type": "microsoft.graph.allDevicesAssignmentTarget",
        "deviceAndAppManagementAssignmentFilterId": "String",
        "deviceAndAppManagementAssignmentFilterType": "String"
      }
    }
  ],
  "androidEnrollmentAssignments": [
    {
      "@odata.type": "microsoft.graph.complianceManagementPartnerAssignment",
      "target": {
        "@odata.type": "microsoft.graph.allDevicesAssignmentTarget",
        "deviceAndAppManagementAssignmentFilterId": "String",
        "deviceAndAppManagementAssignmentFilterType": "String"
      }
    }
  ],
  "iosEnrollmentAssignments": [
    {
      "@odata.type": "microsoft.graph.complianceManagementPartnerAssignment",
      "target": {
        "@odata.type": "microsoft.graph.allDevicesAssignmentTarget",
        "deviceAndAppManagementAssignmentFilterId": "String",
        "deviceAndAppManagementAssignmentFilterType": "String"
      }
    }
  ]
}
```




