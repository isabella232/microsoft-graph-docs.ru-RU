---
title: Тип ресурса Йомиперсоннаме
description: Тип ресурса Йомиперсоннаме
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: resourcePageType
ms.openlocfilehash: 926479832db04e427e7ca1d73744008db7dc6aaa
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48079629"
---
# <a name="yomipersonname-resource-type"></a>Тип ресурса Йомиперсоннаме

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Предоставляет пользователю способ хранения сведений о том, как произношение имени для несобственных динамиков языка, в котором представлен ресурс [PersonName](personname.md) .

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание                                             |
|:-------------|:------------|:--------------------------------------------------------|
|displayName   |String       | Составные руководства по произношению имени и фамилии.  |
|первыми         |String       | Произношение руководства для первого имени пользователя.     |
|Фамили          |String       | Произношение руководства для последнего имени пользователя.      |
|маиден        |String       | Произношение руководства для маиден имени пользователя.    |
|назван        |String       | Произношение руководства по среднему имени пользователя.    |

## <a name="relationships"></a>Отношения

Отсутствуют.

## <a name="json-representation"></a>Представление в формате JSON

Ниже указано представление ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yomiPersonName"
}
-->

``` json

{
  "displayName": "String",
  "first": "String",
  "maiden": "String",
  "middle": "String",
  "last": "String"
}
```


