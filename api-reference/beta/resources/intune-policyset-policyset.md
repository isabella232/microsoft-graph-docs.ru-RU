---
title: Тип ресурса "политика"
description: Класс, содержащий свойства, используемые для объекта Policy.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 5aa43500fc2adf9f44ba3bec00cb6c1315fab574
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2019
ms.locfileid: "37201257"
---
# <a name="policyset-resource-type"></a>Тип ресурса "политика"

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Класс, содержащий свойства, используемые для объекта Policy.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список Полицисетс](../api/intune-policyset-policyset-list.md)|Коллекция набора [политик](../resources/intune-policyset-policyset.md)|Список свойств и связей объектов набора [политик](../resources/intune-policyset-policyset.md) .|
|[Получение политики](../api/intune-policyset-policyset-get.md)|[групповой политики](../resources/intune-policyset-policyset.md)|Чтение свойств и связей объекта набора [политик](../resources/intune-policyset-policyset.md) .|
|[Создание политики](../api/intune-policyset-policyset-create.md)|[групповой политики](../resources/intune-policyset-policyset.md)|Создайте новый объект [Policy](../resources/intune-policyset-policyset.md) .|
|[Удаление политики](../api/intune-policyset-policyset-delete.md)|Нет|Удаляет набор [политик](../resources/intune-policyset-policyset.md).|
|[Обновление политики](../api/intune-policyset-policyset-update.md)|[групповой политики](../resources/intune-policyset-policyset.md)|Обновление свойств объекта набора [политик](../resources/intune-policyset-policyset.md) .|
|[действие обновления](../api/intune-policyset-policyset-update.md)|Нет|Н/Д|
|[действие Жетполицисетс](../api/intune-policyset-policyset-getpolicysets.md)|Коллекция набора [политик](../resources/intune-policyset-policyset.md)|Н/Д|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Ключ набора политик.|
|createdDateTime|DateTimeOffset|Время создания набора политик.|
|lastModifiedDateTime|DateTimeOffset|Время последнего изменения набора политик.|
|displayName|Строка|DisplayName набора политик.|
|description|String|Описание набора политик.|
|status|[полицисетстатус](../resources/intune-policyset-policysetstatus.md)|Состояние проверки или назначения набора политик. Возможные значения: `unknown`, `validating`, `partialSuccess`, `success`, `error`, `notAssigned`.|
|errorCode|[Коде](../resources/intune-policyset-errorcode.md)|Код ошибки (при возникновении ошибки). Возможные значения: `noError`, `unauthorized`, `notFound`, `deleted`.|
|гуидеддеплойменттагс|Коллекция строк|Теги в руководстве по развертыванию|
|roleScopeTags|Коллекция строк|RoleScopeTags набора политик|

## <a name="relationships"></a>Отношения
|Отношение|Тип|Описание|
|:---|:---|:---|
|assignments|Коллекция [полицисетассигнмент](../resources/intune-policyset-policysetassignment.md)|Назначения набора политик.|
|items|Коллекция [полицисетитем](../resources/intune-policyset-policysetitem.md)|Элементы набора политик с максимальным количеством 100.|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.policySet"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.policySet",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "description": "String",
  "status": "String",
  "errorCode": "String",
  "guidedDeploymentTags": [
    "String"
  ],
  "roleScopeTags": [
    "String"
  ]
}
```


