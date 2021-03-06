---
title: Тип ресурса Усерекспериенцеаналитиксапфеалсосверсионперформанце
description: Сущность производительности "версия ОС" для устройства аналитики взаимодействия с пользователем содержит сведения о производительности версий ОС.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 404d40b0924b78eec5a0690fe4986421f84c05f2
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49208480"
---
# <a name="userexperienceanalyticsapphealthosversionperformance-resource-type"></a>Тип ресурса Усерекспериенцеаналитиксапфеалсосверсионперформанце

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Сущность производительности "версия ОС" для устройства аналитики взаимодействия с пользователем содержит сведения о производительности версий ОС.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список Усерекспериенцеаналитиксапфеалсосверсионперформанцес](../api/intune-devices-userexperienceanalyticsapphealthosversionperformance-list.md)|Коллекция [усерекспериенцеаналитиксапфеалсосверсионперформанце](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md)|Список свойств и связей объектов [усерекспериенцеаналитиксапфеалсосверсионперформанце](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md) .|
|[Получение Усерекспериенцеаналитиксапфеалсосверсионперформанце](../api/intune-devices-userexperienceanalyticsapphealthosversionperformance-get.md)|[userExperienceAnalyticsAppHealthOSVersionPerformance](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md)|Чтение свойств и связей объекта [усерекспериенцеаналитиксапфеалсосверсионперформанце](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md) .|
|[Создание Усерекспериенцеаналитиксапфеалсосверсионперформанце](../api/intune-devices-userexperienceanalyticsapphealthosversionperformance-create.md)|[userExperienceAnalyticsAppHealthOSVersionPerformance](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md)|Создание нового объекта [усерекспериенцеаналитиксапфеалсосверсионперформанце](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md) .|
|[Удаление Усерекспериенцеаналитиксапфеалсосверсионперформанце](../api/intune-devices-userexperienceanalyticsapphealthosversionperformance-delete.md)|Нет|Удаляет объект [усерекспериенцеаналитиксапфеалсосверсионперформанце](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md).|
|[Обновление Усерекспериенцеаналитиксапфеалсосверсионперформанце](../api/intune-devices-userexperienceanalyticsapphealthosversionperformance-update.md)|[userExperienceAnalyticsAppHealthOSVersionPerformance](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md)|Обновление свойств объекта [усерекспериенцеаналитиксапфеалсосверсионперформанце](../resources/intune-devices-userexperienceanalyticsapphealthosversionperformance.md) .|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Уникальный идентификатор объекта производительности для версии службы аналитики взаимодействия с пользователем.|
|osVersion|String|Версия ОС, установленная на устройстве.|
|осбуилднумбер|String|Номер сборки ОС, установленный на устройстве.|
|активедевицекаунт|Int32|Число активных устройств для версии ОС. Допустимые значения: от 2147483648 до 2147483647|
|меантиметофаилуреинминутес|Int32|Среднее время до сбоя для версии ОС в минутах. Допустимые значения: от 2147483648 до 2147483647|
|осверсионапфеалсскоре|Двойное с плавающей точкой|Показатель работоспособности приложения для версии ОС. Допустимые значения — 1 79769313486232e308 E + 308 — 1 79769313486232e308 E + 308|
|осверсионапфеалсстатус|String|Общее состояние работоспособности приложения для версии ОС.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.userExperienceAnalyticsAppHealthOSVersionPerformance"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthOSVersionPerformance",
  "id": "String (identifier)",
  "osVersion": "String",
  "osBuildNumber": "String",
  "activeDeviceCount": 1024,
  "meanTimeToFailureInMinutes": 1024,
  "osVersionAppHealthScore": "4.2",
  "osVersionAppHealthStatus": "String"
}
```




