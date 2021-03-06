---
title: Тип ресурса servicePlanInfo
description: Содержит сведения о плане обслуживания, связанном с подписанным SKU. Свойство **servicePlans** объекта subscribedSku представляет собой коллекцию объектов **servicePlanInfo**.
localization_priority: Normal
author: krbain
ms.prod: ''
doc_type: resourcePageType
ms.openlocfilehash: 6176174a046618176627e8bbe7b8a984c58a3c22
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47991861"
---
# <a name="serviceplaninfo-resource-type"></a>Тип ресурса servicePlanInfo

Пространство имен: microsoft.graph

Содержит сведения о плане обслуживания, связанном с подписанным SKU. Свойство **servicePlans** объекта [subscribedSku](subscribedsku.md) представляет собой коллекцию объектов **servicePlanInfo**.


## <a name="properties"></a>Свойства
| Свойство     | Тип   |Описание|
|:---------------|:--------|:----------|
|сервицепланид|Guid|Уникальный идентификатор плана обслуживания.|
|сервицепланнаме|String|Имя плана обслуживания.|
|provisioningStatus|String|Состояние подготовки плана обслуживания. Возможные значения:<br/>"Success" — служба полностью подготовлена.<br/>"Disabled" — служба отключена.<br/>"PendingInput" — служба еще не подготовлена; ожидается подтверждение службы.<br/>"Пендингактиватион" — служба подготовлена, но требует явной активации администратором (например, Intune_O365 план обслуживания).<br/>"Пендингпровисионинг" — Корпорация Майкрософт добавила новую службу в SKU продукта и еще не активировалась в клиенте.|
|Тег|String|Объект, которому можно назначить план обслуживания. Возможные значения:<br/>"User" — план обслуживания можно назначить отдельным пользователям.<br/>"Company" — план обслуживания можно назначить всему клиенту.|

## <a name="json-representation"></a>Представление JSON

Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.servicePlanInfo"
}-->

```json
{
  "appliesTo": "string",
  "provisioningStatus": "string",
  "servicePlanId": "guid",
  "servicePlanName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "servicePlanInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

