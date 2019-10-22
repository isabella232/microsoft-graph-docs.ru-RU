---
title: Тип ресурса Граупполицимигратионрепорт
description: Отчет о миграции групповой политики.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 038c0f81999bebbf0d2406637bb71e03a67397ce
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2019
ms.locfileid: "37539206"
---
# <a name="grouppolicymigrationreport-resource-type"></a>Тип ресурса Граупполицимигратионрепорт

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Отчет о миграции групповой политики.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список Граупполицимигратионрепортс](../api/intune-gpanalyticsservice-grouppolicymigrationreport-list.md)|Коллекция [граупполицимигратионрепорт](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md)|Список свойств и связей объектов [граупполицимигратионрепорт](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) .|
|[Получение Граупполицимигратионрепорт](../api/intune-gpanalyticsservice-grouppolicymigrationreport-get.md)|[граупполицимигратионрепорт](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md)|Чтение свойств и связей объекта [граупполицимигратионрепорт](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) .|
|[Создание Граупполицимигратионрепорт](../api/intune-gpanalyticsservice-grouppolicymigrationreport-create.md)|[граупполицимигратионрепорт](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md)|Создание нового объекта [граупполицимигратионрепорт](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) .|
|[Удаление Граупполицимигратионрепорт](../api/intune-gpanalyticsservice-grouppolicymigrationreport-delete.md)|Нет|Удаляет объект [граупполицимигратионрепорт](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md).|
|[Обновление Граупполицимигратионрепорт](../api/intune-gpanalyticsservice-grouppolicymigrationreport-update.md)|[граупполицимигратионрепорт](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md)|Обновление свойств объекта [граупполицимигратионрепорт](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) .|
|[действие Креатемигратионрепорт](../api/intune-gpanalyticsservice-grouppolicymigrationreport-createmigrationreport.md)|String|Н/Д|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Пока не задокументировано.|
|граупполициобжектид|GUID|GUID объекта групповой политики из XML-содержимого объекта групповой политики|
|displayName|Строка|Имя объекта групповой политики из XML-содержимого объекта групповой политики|
|аудистингуишеднаме|String|Различающееся имя подразделения.|
|createdDateTime|DateTimeOffset|Дата и время создания Граупполицимигратионрепорт.|
|lastModifiedDateTime|DateTimeOffset|Дата и время последнего изменения Граупполицимигратионрепорт.|
|граупполицикреатеддатетиме|DateTimeOffset|Дата и время создания Граупполицимигратионрепорт.|
|граупполициластмодифиеддатетиме|DateTimeOffset|Дата и время последнего изменения Граупполицимигратионрепорт.|
|мигратионреадинесс|[граупполицимигратионреадинесс](../resources/intune-gpanalyticsservice-grouppolicymigrationreadiness.md)|Область действия Intune для связанного файлового объекта групповой политики. Возможные значения: `none`, `partial`, `complete`, `error`, `notApplicable`.|
|таржетединактиведиректори|Логический|Свойство Targeted в Active Directory из XML-контента объекта групповой политики|
|тоталсеттингскаунт|Int32|Общее количество параметров групповой политики из файла GPO.|
|суппортедсеттингскаунт|Int32|Количество параметров групповой политики, поддерживаемых Intune.|
|суппортедсеттингсперцент|Int32|Процент параметров групповой политики, поддерживаемых Intune.|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|граупполицисеттингмаппингс|Коллекция [граупполицисеттингмаппинг](../resources/intune-gpanalyticsservice-grouppolicysettingmapping.md)|Список параметров групповой политики для сопоставлений MDM/Intune.|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.groupPolicyMigrationReport"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.groupPolicyMigrationReport",
  "id": "String (identifier)",
  "groupPolicyObjectId": "Guid",
  "displayName": "String",
  "ouDistinguishedName": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "groupPolicyCreatedDateTime": "String (timestamp)",
  "groupPolicyLastModifiedDateTime": "String (timestamp)",
  "migrationReadiness": "String",
  "targetedInActiveDirectory": true,
  "totalSettingsCount": 1024,
  "supportedSettingsCount": 1024,
  "supportedSettingsPercent": 1024
}
```


