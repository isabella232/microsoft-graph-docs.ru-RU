---
title: Тип ресурса managedAppOperation
description: Представляет операцию, примененную к регистрации приложения.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 5ad689737da4944f973c813615ddc2b0cb2f8c1f
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49302644"
---
# <a name="managedappoperation-resource-type"></a>Тип ресурса managedAppOperation

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Представляет операцию, примененную к регистрации приложения.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список объектов List managedAppOperation](../api/intune-mam-managedappoperation-list.md)|Коллекция [managedAppOperation](../resources/intune-mam-managedappoperation.md)|Список свойств и связей объектов [managedAppOperation](../resources/intune-mam-managedappoperation.md).|
|[Получение объекта managedAppOperation](../api/intune-mam-managedappoperation-get.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md)|Чтение свойств и связей объекта [managedAppOperation](../resources/intune-mam-managedappoperation.md).|
|[Создание объекта managedAppOperation](../api/intune-mam-managedappoperation-create.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md)|Создание объекта [managedAppOperation](../resources/intune-mam-managedappoperation.md).|
|[Удаление объекта managedAppOperation](../api/intune-mam-managedappoperation-delete.md)|Нет|Удаляет объекта [managedAppOperation](../resources/intune-mam-managedappoperation.md).|
|[Обновление объекта managedAppOperation](../api/intune-mam-managedappoperation-update.md)|[managedAppOperation](../resources/intune-mam-managedappoperation.md)|Обновление свойств объекта [managedAppOperation](../resources/intune-mam-managedappoperation.md).|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|displayName|String|Имя операции.|
|lastModifiedDateTime|DateTimeOffset|Время последнего изменения операции для приложения.|
|state|String|Текущее состояние операции|
|id|String|Ключ объекта.|
|version|String|Версия объекта.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppOperation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppOperation",
  "displayName": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "state": "String",
  "id": "String (identifier)",
  "version": "String"
}
```




