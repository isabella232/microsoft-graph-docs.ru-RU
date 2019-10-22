---
title: Тип ресурса Усерекспериенцеаналитиксдевицестартуфистори
description: Сущность журнала запуска устройства Analytics User Experience содержит подробные сведения о журнале производительности загрузки устройств.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: e9178f62d1dd711134ba1925a6cc5c4a9082a99e
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2019
ms.locfileid: "37538464"
---
# <a name="userexperienceanalyticsdevicestartuphistory-resource-type"></a>Тип ресурса Усерекспериенцеаналитиксдевицестартуфистори

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Сущность журнала запуска устройства Analytics User Experience содержит подробные сведения о журнале производительности загрузки устройств.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список Усерекспериенцеаналитиксдевицестартуфисториес](../api/intune-devices-userexperienceanalyticsdevicestartuphistory-list.md)|Коллекция [усерекспериенцеаналитиксдевицестартуфистори](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md)|Список свойств и связей объектов [усерекспериенцеаналитиксдевицестартуфистори](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) .|
|[Получение Усерекспериенцеаналитиксдевицестартуфистори](../api/intune-devices-userexperienceanalyticsdevicestartuphistory-get.md)|[усерекспериенцеаналитиксдевицестартуфистори](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md)|Чтение свойств и связей объекта [усерекспериенцеаналитиксдевицестартуфистори](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) .|
|[Создание Усерекспериенцеаналитиксдевицестартуфистори](../api/intune-devices-userexperienceanalyticsdevicestartuphistory-create.md)|[усерекспериенцеаналитиксдевицестартуфистори](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md)|Создание нового объекта [усерекспериенцеаналитиксдевицестартуфистори](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) .|
|[Удаление Усерекспериенцеаналитиксдевицестартуфистори](../api/intune-devices-userexperienceanalyticsdevicestartuphistory-delete.md)|Нет|Удаляет объект [усерекспериенцеаналитиксдевицестартуфистори](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md).|
|[Обновление Усерекспериенцеаналитиксдевицестартуфистори](../api/intune-devices-userexperienceanalyticsdevicestartuphistory-update.md)|[усерекспериенцеаналитиксдевицестартуфистори](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md)|Обновление свойств объекта [усерекспериенцеаналитиксдевицестартуфистори](../resources/intune-devices-userexperienceanalyticsdevicestartuphistory.md) .|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Уникальный идентификатор журнала запуска устройства Analytics User Experience.|
|deviceId|String|Идентификатор устройства службы аналитики взаимодействия с пользователем.|
|startTime|DateTimeOffset|Время начала загрузки устройства Analytics User Experience.|
|коребуттимеинмс|Int32|Время загрузки ядра устройства аналитики для пользователя (в миллисекундах).|
|граупполицибуттимеинмс|Int32|Время загрузки групповой политики устройства Analytics для пользователя (в миллисекундах).|
|феатуреупдатебуттимеинмс|Int32|Время обновления компонента службы аналитики взаимодействия с пользователем (в миллисекундах).|
|тоталбуттимеинмс|Int32|Общее время загрузки устройства Analytics User Experience (в миллисекундах).|
|граупполицилогинтимеинмс|Int32|Время входа в групповую политику устройства Analytics User Experience (в миллисекундах).|
|корелогинтимеинмс|Int32|Время входа в ядро устройства аналитики взаимодействия с пользователем (в миллисекундах).|
|тоталлогинтимеинмс|Int32|Общее время входа в систему для устройства аналитики взаимодействия с пользователем (в миллисекундах).|
|исфирстлогин|Логический|Первое имя входа устройства Analytics User Experience.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.userExperienceAnalyticsDeviceStartupHistory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsDeviceStartupHistory",
  "id": "String (identifier)",
  "deviceId": "String",
  "startTime": "String (timestamp)",
  "coreBootTimeInMs": 1024,
  "groupPolicyBootTimeInMs": 1024,
  "featureUpdateBootTimeInMs": 1024,
  "totalBootTimeInMs": 1024,
  "groupPolicyLoginTimeInMs": 1024,
  "coreLoginTimeInMs": 1024,
  "totalLoginTimeInMs": 1024,
  "isFirstLogin": true
}
```


