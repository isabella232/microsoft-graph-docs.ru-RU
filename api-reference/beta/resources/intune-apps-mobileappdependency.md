---
title: Тип ресурса Мобилеаппдепенденци
description: Описывает тип зависимости между двумя мобильными приложениями.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 525e094350a3ce255d0a695ad2631485087e3d37
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49280960"
---
# <a name="mobileappdependency-resource-type"></a>Тип ресурса Мобилеаппдепенденци

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Описывает тип зависимости между двумя мобильными приложениями.


Наследуется от [мобилеаппрелатионшип](../resources/intune-apps-mobileapprelationship.md)

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список МобилеаппдепенденЦиес](../api/intune-apps-mobileappdependency-list.md)|Коллекция [мобилеаппдепенденци](../resources/intune-apps-mobileappdependency.md)|Список свойств и связей объектов [мобилеаппдепенденци](../resources/intune-apps-mobileappdependency.md) .|
|[Получение Мобилеаппдепенденци](../api/intune-apps-mobileappdependency-get.md)|[mobileAppDependency](../resources/intune-apps-mobileappdependency.md)|Чтение свойств и связей объекта [мобилеаппдепенденци](../resources/intune-apps-mobileappdependency.md) .|
|[Создание Мобилеаппдепенденци](../api/intune-apps-mobileappdependency-create.md)|[mobileAppDependency](../resources/intune-apps-mobileappdependency.md)|Создание нового объекта [мобилеаппдепенденци](../resources/intune-apps-mobileappdependency.md) .|
|[Удаление Мобилеаппдепенденци](../api/intune-apps-mobileappdependency-delete.md)|Нет|Удаляет объект [мобилеаппдепенденци](../resources/intune-apps-mobileappdependency.md).|
|[Обновление Мобилеаппдепенденци](../api/intune-apps-mobileappdependency-update.md)|[mobileAppDependency](../resources/intune-apps-mobileappdependency.md)|Обновление свойств объекта [мобилеаппдепенденци](../resources/intune-apps-mobileappdependency.md) .|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Идентификатор сущности отношения. Наследуется от [мобилеаппрелатионшип](../resources/intune-apps-mobileapprelationship.md)|
|targetId|String|Идентификатор приложения целевого приложения для мобильных устройств. Наследуется от [мобилеаппрелатионшип](../resources/intune-apps-mobileapprelationship.md)|
|таржетдисплайнаме|String|Отображаемое имя целевого мобильного приложения. Наследуется от [мобилеаппрелатионшип](../resources/intune-apps-mobileapprelationship.md)|
|таржетдисплайверсион|String|Версия отображения целевого мобильного приложения. Наследуется от [мобилеаппрелатионшип](../resources/intune-apps-mobileapprelationship.md)|
|таржетпублишер|String|Издатель целевого мобильного приложения. Наследуется от [мобилеаппрелатионшип](../resources/intune-apps-mobileapprelationship.md)|
|targetType|[mobileAppRelationshipType](../resources/intune-apps-mobileapprelationshiptype.md)|Тип связи, указывающий, является ли целевой объект родительским или дочерним. Наследуется от [мобилеаппрелатионшип](../resources/intune-apps-mobileapprelationship.md). Возможные значения: `child`, `parent`.|
|депенденцитипе|[mobileAppDependencyType](../resources/intune-apps-mobileappdependencytype.md)|Тип отношения зависимости между родительским и дочерним приложениями. Возможные значения: `detect`, `autoInstall`.|
|депендентаппкаунт|Int32|Общее количество зависимостей для дочернего приложения.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppDependency"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppDependency",
  "id": "String (identifier)",
  "targetId": "String",
  "targetDisplayName": "String",
  "targetDisplayVersion": "String",
  "targetPublisher": "String",
  "targetType": "String",
  "dependencyType": "String",
  "dependentAppCount": 1024
}
```




