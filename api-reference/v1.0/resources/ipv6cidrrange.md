---
title: Тип ресурса iPv6CidrRange
description: Представляет диапазон IPv6-адресов с использованием нотации CIDR.
localization_priority: Normal
author: videor
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 75c15484a310bdff66052b9381bea8b62779979c
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47967459"
---
# <a name="ipv6cidrrange-resource-type"></a>Тип ресурса iPv6CidrRange

Пространство имен: microsoft.graph

Представляет диапазон IPv6-адресов с использованием нотации CIDR.

Наследуется от ресурса [ipRange](../resources/iprange.md)

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|Цидраддресс|String|IPv6-адрес в нотации CIDR|

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.iPv6CidrRange",
  "baseType": "microsoft.graph.ipRange"
}-->

```json
{
  "cidrAddress": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "iPv6CidrRange resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
