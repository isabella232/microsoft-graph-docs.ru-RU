---
title: Тип ресурса Девицеманажементексчанжеонпремисесполици
description: Одноэлементный объект, представляющий политику локальной политики Exchange, настроенную для клиента.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 1df2411b46e5e8e01482d2e7bec6216d40f520b0
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49256143"
---
# <a name="devicemanagementexchangeonpremisespolicy-resource-type"></a>Тип ресурса Девицеманажементексчанжеонпремисесполици

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Одноэлементный объект, представляющий политику локальной политики Exchange, настроенную для клиента.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Получение Девицеманажементексчанжеонпремисесполици](../api/intune-onboarding-devicemanagementexchangeonpremisespolicy-get.md)|[девицеманажементексчанжеонпремисесполици](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md)|Чтение свойств и связей объекта [девицеманажементексчанжеонпремисесполици](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) .|
|[Обновление Девицеманажементексчанжеонпремисесполици](../api/intune-onboarding-devicemanagementexchangeonpremisespolicy-update.md)|[девицеманажементексчанжеонпремисесполици](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md)|Обновление свойств объекта [девицеманажементексчанжеонпремисесполици](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) .|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Пока не задокументировано.|
|нотификатионконтент|Binary|Текст уведомления, который будет отправляться пользователям, помещенным в карантин этой политикой. Это HTML-кодированный массив байтов в кодировке UTF8.|
|дефаултакцесслевел|[девицеманажементексчанжеакцесслевел](../resources/intune-onboarding-devicemanagementexchangeaccesslevel.md)|Состояние доступа по умолчанию в Exchange. Это правило применяется глобально ко всей организации Exchange. Возможные значения: `none`, `allow`, `block`, `quarantine`.|
|акцессрулес|Коллекция [девицеманажементексчанжеакцессруле](../resources/intune-onboarding-devicemanagementexchangeaccessrule.md)|Список правил доступа к устройствам в Exchange. Правила доступа применяются глобально ко всей организации Exchange|
|кновндевицеклассес|Коллекция [девицеманажементексчанжедевицекласс](../resources/intune-onboarding-devicemanagementexchangedeviceclass.md)|Список классов устройств, известных для Exchange|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|conditionalAccessSettings|[onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md)|Параметры локального условного доступа в Exchange. Для локального условного доступа устройства должны быть зарегистрированы для доступа к почте и поддерживать его.|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementExchangeOnPremisesPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementExchangeOnPremisesPolicy",
  "id": "String (identifier)",
  "notificationContent": "binary",
  "defaultAccessLevel": "String",
  "accessRules": [
    {
      "@odata.type": "microsoft.graph.deviceManagementExchangeAccessRule",
      "deviceClass": {
        "@odata.type": "microsoft.graph.deviceManagementExchangeDeviceClass",
        "name": "String",
        "type": "String"
      },
      "accessLevel": "String"
    }
  ],
  "knownDeviceClasses": [
    {
      "@odata.type": "microsoft.graph.deviceManagementExchangeDeviceClass",
      "name": "String",
      "type": "String"
    }
  ]
}
```




