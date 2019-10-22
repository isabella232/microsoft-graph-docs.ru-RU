---
title: Тип ресурса Виндовсдефендераппликатионконтролсупплементалполици
description: Пока не задокументировано.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 53edcd8f5f6de071c9bf694858219388bea5002b
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2019
ms.locfileid: "37539129"
---
# <a name="windowsdefenderapplicationcontrolsupplementalpolicy-resource-type"></a>Тип ресурса Виндовсдефендераппликатионконтролсупплементалполици

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Н/Д

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список ВиндовсдефендераппликатионконтролсупплементалполиЦиес](../api/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy-list.md)|Коллекция [виндовсдефендераппликатионконтролсупплементалполици](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md)|Список свойств и связей объектов [виндовсдефендераппликатионконтролсупплементалполици](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md) .|
|[Получение Виндовсдефендераппликатионконтролсупплементалполици](../api/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy-get.md)|[виндовсдефендераппликатионконтролсупплементалполици](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md)|Чтение свойств и связей объекта [виндовсдефендераппликатионконтролсупплементалполици](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md) .|
|[Создание Виндовсдефендераппликатионконтролсупплементалполици](../api/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy-create.md)|[виндовсдефендераппликатионконтролсупплементалполици](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md)|Создание нового объекта [виндовсдефендераппликатионконтролсупплементалполици](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md) .|
|[Удаление Виндовсдефендераппликатионконтролсупплементалполици](../api/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy-delete.md)|Нет|Удаляет объект [виндовсдефендераппликатионконтролсупплементалполици](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md).|
|[Обновление Виндовсдефендераппликатионконтролсупплементалполици](../api/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy-update.md)|[виндовсдефендераппликатионконтролсупплементалполици](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md)|Обновление свойств объекта [виндовсдефендераппликатионконтролсупплементалполици](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy.md) .|
|[Действие assign](../api/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicy-assign.md)|Нет|Пока не задокументировано|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Ключ для дополнительной политики Виндовсдефендераппликатионконтрол.|
|displayName|Строка|Отображаемое имя дополнительной политики Виндовсдефендераппликатионконтрол.|
|description|String|Описание дополнительной политики Виндовсдефендераппликатионконтрол.|
|содержимое|Binary|Содержимое дополнительной политики Виндовсдефендераппликатионконтрол в формате массива байтов.|
|контентфиленаме|String|Имя файла дополнительной политики Виндовсдефендераппликатионконтрол.|
|version|String|Версия дополнительной политики Виндовсдефендераппликатионконтрол.|
|креатиондатетиме|DateTimeOffset|Дата и время отправки дополнительной политики Виндовсдефендераппликатионконтрол.|
|lastModifiedDateTime|DateTimeOffset|Дата и время последнего изменения дополнительной политики Виндовсдефендераппликатионконтрол.|
|roleScopeTagIds|Коллекция String|Список тегов областей для данной дополнительной политики Виндовсдефендераппликатионконтрол.|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|assignments|Коллекция [виндовсдефендераппликатионконтролсупплементалполициассигнмент](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicyassignment.md)|Связанные назначения группы для этой дополнительной политики Виндовсдефендераппликатионконтрол.|
|деплойсуммари|[виндовсдефендераппликатионконтролсупплементалполицидеплойментсуммари](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicydeploymentsummary.md)|Дополнительные сведения о развертывании дополнительной политики Виндовсдефендераппликатионконтрол.|
|deviceStatuses|Коллекция [виндовсдефендераппликатионконтролсупплементалполицидеплойментстатус](../resources/intune-unlock-windowsdefenderapplicationcontrolsupplementalpolicydeploymentstatus.md)|Список состояний развертывания устройств для этой дополнительной политики Виндовсдефендераппликатионконтрол.|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsDefenderApplicationControlSupplementalPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsDefenderApplicationControlSupplementalPolicy",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "content": "binary",
  "contentFileName": "String",
  "version": "String",
  "creationDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "roleScopeTagIds": [
    "String"
  ]
}
```


