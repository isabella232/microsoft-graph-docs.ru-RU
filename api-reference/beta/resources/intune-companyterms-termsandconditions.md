---
title: Тип ресурса termsAndConditions
description: Объект termsAndConditions представляет метаданные и содержимое определенной политики условий. Содержимое политик условий предоставляется пользователю при первой попытке регистрации в Intune, а после этого — при правках, которые нужно повторно принять по требованию администратора. Благодаря им администраторы могут огласить условия, с которыми должен согласиться пользователь для регистрации устройств в Intune.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: bdc4f6d65952250534bcacbbaf616ad302ed2498
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49289050"
---
# <a name="termsandconditions-resource-type"></a>Тип ресурса termsAndConditions

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Объект termsAndConditions представляет метаданные и содержимое определенной политики условий. Содержимое политик условий предоставляется пользователю при первой попытке регистрации в Intune, а после этого — при правках, которые нужно повторно принять по требованию администратора. Благодаря им администраторы могут огласить условия, с которыми должен согласиться пользователь для регистрации устройств в Intune.

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Перечисление объектов termsAndConditions](../api/intune-companyterms-termsandconditions-list.md)|Коллекция объектов [termsAndConditions](../resources/intune-companyterms-termsandconditions.md)|Список свойств и связей объектов [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).|
|[Получение объекта termsAndConditions](../api/intune-companyterms-termsandconditions-get.md)|[termsAndConditions](../resources/intune-companyterms-termsandconditions.md)|Чтение свойств и связей объекта [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).|
|[Создание объекта termsAndConditions](../api/intune-companyterms-termsandconditions-create.md)|[termsAndConditions](../resources/intune-companyterms-termsandconditions.md)|Создание объекта [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).|
|[Удаление объекта termsAndConditions](../api/intune-companyterms-termsandconditions-delete.md)|Нет|Удаление объекта [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).|
|[Обновление объекта termsAndConditions](../api/intune-companyterms-termsandconditions-update.md)|[termsAndConditions](../resources/intune-companyterms-termsandconditions.md)|Обновление свойств объекта [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Уникальный идентификатор политики использования.|
|createdDateTime|DateTimeOffset|Дата и время создания объекта.|
|modifiedDateTime|DateTimeOffset|Дата и время последнего изменения объекта.|
|lastModifiedDateTime|DateTimeOffset|Дата и время последнего изменения объекта.|
|displayName|String|Имя политики использования, указанное администратором. |
|description|String|Описание политики использования, указанное администратором.|
|title|String|Название условий, указанное администратором. Показывается пользователю при запросе на принятие политики использования.|
|bodyText|String|Основной текст условий, заданный администратором (как правило, сами условия). Показывается пользователю при запросе на принятие политики использования.|
|acceptanceStatement|String|Указанное администратором объяснение условий. Как правило, пользователю объясняется, с чем связано принятие условий, изложенных в соответствующей политике. Показывается пользователю при запросе на принятие политики использования.|
|version|Int32|Целое число, указывающее текущую версию условий. Увеличивается, когда администратор вносит изменения в условия и хочет, чтобы пользователи повторно приняли измененную политику.|
|roleScopeTagIds|Коллекция строк|Список тегов областей для этого экземпляра сущности.|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|groupAssignments|Коллекция [термсандкондитионсграупассигнмент](../resources/intune-companyterms-termsandconditionsgroupassignment.md)|Список назначений групп для этой политики T&C.|
|assignments|Коллекция объектов [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md)|Список назначений для этой политики условий.|
|acceptanceStatuses|Коллекция объектов [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md)|Список состояний принятия для этой политики условий.|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termsAndConditions"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.termsAndConditions",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "description": "String",
  "title": "String",
  "bodyText": "String",
  "acceptanceStatement": "String",
  "version": 1024,
  "roleScopeTagIds": [
    "String"
  ]
}
```




