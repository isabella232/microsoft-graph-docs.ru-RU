---
title: Тип ресурса Виндовсфеатуреупдатепрофиле
description: Профиль обновления компонентов Windows
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 4806f33f753560739c9ced128c64d3a626b9b03a
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2019
ms.locfileid: "37201189"
---
# <a name="windowsfeatureupdateprofile-resource-type"></a>Тип ресурса Виндовсфеатуреупдатепрофиле

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Профиль обновления компонентов Windows

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список Виндовсфеатуреупдатепрофилес](../api/intune-softwareupdate-windowsfeatureupdateprofile-list.md)|Коллекция [виндовсфеатуреупдатепрофиле](../resources/intune-softwareupdate-windowsfeatureupdateprofile.md)|Список свойств и связей объектов [виндовсфеатуреупдатепрофиле](../resources/intune-softwareupdate-windowsfeatureupdateprofile.md) .|
|[Получение Виндовсфеатуреупдатепрофиле](../api/intune-softwareupdate-windowsfeatureupdateprofile-get.md)|[виндовсфеатуреупдатепрофиле](../resources/intune-softwareupdate-windowsfeatureupdateprofile.md)|Чтение свойств и связей объекта [виндовсфеатуреупдатепрофиле](../resources/intune-softwareupdate-windowsfeatureupdateprofile.md) .|
|[Создание Виндовсфеатуреупдатепрофиле](../api/intune-softwareupdate-windowsfeatureupdateprofile-create.md)|[виндовсфеатуреупдатепрофиле](../resources/intune-softwareupdate-windowsfeatureupdateprofile.md)|Создание нового объекта [виндовсфеатуреупдатепрофиле](../resources/intune-softwareupdate-windowsfeatureupdateprofile.md) .|
|[Удаление Виндовсфеатуреупдатепрофиле](../api/intune-softwareupdate-windowsfeatureupdateprofile-delete.md)|Нет|Удаляет объект [виндовсфеатуреупдатепрофиле](../resources/intune-softwareupdate-windowsfeatureupdateprofile.md).|
|[Обновление Виндовсфеатуреупдатепрофиле](../api/intune-softwareupdate-windowsfeatureupdateprofile-update.md)|[виндовсфеатуреупдатепрофиле](../resources/intune-softwareupdate-windowsfeatureupdateprofile.md)|Обновление свойств объекта [виндовсфеатуреупдатепрофиле](../resources/intune-softwareupdate-windowsfeatureupdateprofile.md) .|
|[Действие assign](../api/intune-softwareupdate-windowsfeatureupdateprofile-assign.md)|Нет|Н/Д|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Идентификатор объекта.|
|displayName|Строка|Отображаемое имя профиля.|
|description|String|Описание профиля, указанного пользователем.|
|феатуреупдатеверсион|String.|Версия обновления компонентов, которая будет развернута на устройствах, предназначенных для этого профиля. Версией может быть любая поддерживаемая версия, например 1709, 1803 или 1809 и т. д.|
|createdDateTime|DateTimeOffset|Дата и время создания профиля.|
|lastModifiedDateTime|DateTimeOffset|Дата и время последнего изменения профиля.|

## <a name="relationships"></a>Отношения
|Отношение|Тип|Описание|
|:---|:---|:---|
|assignments|Коллекция [виндовсфеатуреупдатепрофилеассигнмент](../resources/intune-softwareupdate-windowsfeatureupdateprofileassignment.md)|Список назначений групп для профиля.|
|девицеупдатестатес|Коллекция [виндовсупдатестате](../resources/intune-shared-windowsupdatestate.md)|Список состояний устройств, для которых предназначен данный профиль|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsFeatureUpdateProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsFeatureUpdateProfile",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "featureUpdateVersion": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)"
}
```


