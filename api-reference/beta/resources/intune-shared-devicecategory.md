---
title: Тип ресурса deviceCategory
description: Эти категории затем можно применить к устройству в консоли Azure Intune или выбрать во время регистрации устройства пользователем. На основе категорий устройств вы можете фильтровать отчеты и создавать динамические группы устройств Azure Active Directory.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 14ff0efe2532fd808e94c27c68777c4935212b01
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49306900"
---
# <a name="devicecategory-resource-type"></a>Тип ресурса deviceCategory

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Категории устройств обеспечивают способ организации устройств. С помощью категорий устройств Администраторы компании могут определять уникальные категории, которые имеют смысл в своей компании. Эти категории затем можно применить к устройству в консоли Azure Intune или выбрать во время регистрации устройства пользователем. На основе категорий устройств вы можете фильтровать отчеты и создавать динамические группы устройств Azure Active Directory.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Перечисление объектов deviceCategory](../api/intune-shared-devicecategory-list.md)|Коллекция объектов [deviceCategory](../resources/intune-shared-devicecategory.md)|Список свойств и связей объектов [deviceCategory](../resources/intune-shared-devicecategory.md).|
|[Получение объекта deviceCategory](../api/intune-shared-devicecategory-get.md)|[deviceCategory](../resources/intune-shared-devicecategory.md)|Чтение свойств и связей объекта [deviceCategory](../resources/intune-shared-devicecategory.md).|
|[Создание объекта deviceCategory](../api/intune-shared-devicecategory-create.md)|[deviceCategory](../resources/intune-shared-devicecategory.md)|Создание объекта [deviceCategory](../resources/intune-shared-devicecategory.md).|
|[Удаление объекта deviceCategory](../api/intune-shared-devicecategory-delete.md)|Нет|Удаление объекта [deviceCategory](../resources/intune-shared-devicecategory.md).|
|[Обновление объекта deviceCategory](../api/intune-shared-devicecategory-update.md)|[deviceCategory](../resources/intune-shared-devicecategory.md)|Обновление свойств объекта [deviceCategory](../resources/intune-shared-devicecategory.md).|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Уникальный идентификатор категории устройства. Только для чтения.|
|**Адаптация**|
|displayName|String|Отображаемое имя категории устройств.|
|description|String|Необязательное описание категории устройств.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String"
}
```




