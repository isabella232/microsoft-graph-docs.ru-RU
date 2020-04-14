---
title: Тип ресурса Кондитионалакцесссессионконтрол
description: Базовый тип управления сеансом.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 856eaa294916bb47022307e3c2252400033c7461
ms.sourcegitcommit: bbcf074f0be9d5e02f84c290122850cc5968fb1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2020
ms.locfileid: "43442179"
---
# <a name="conditionalaccesssessioncontrol-resource-type"></a><span data-ttu-id="5fef9-103">Тип ресурса Кондитионалакцесссессионконтрол</span><span class="sxs-lookup"><span data-stu-id="5fef9-103">conditionalAccessSessionControl resource type</span></span>

<span data-ttu-id="5fef9-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="5fef9-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="5fef9-105">Базовый тип управления сеансом.</span><span class="sxs-lookup"><span data-stu-id="5fef9-105">Session control base type.</span></span>

## <a name="properties"></a><span data-ttu-id="5fef9-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="5fef9-106">Properties</span></span>

| <span data-ttu-id="5fef9-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="5fef9-107">Property</span></span>     | <span data-ttu-id="5fef9-108">Тип</span><span class="sxs-lookup"><span data-stu-id="5fef9-108">Type</span></span>        | <span data-ttu-id="5fef9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5fef9-109">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="5fef9-110">isEnabled</span><span class="sxs-lookup"><span data-stu-id="5fef9-110">isEnabled</span></span>     |<span data-ttu-id="5fef9-111">Boolean</span><span class="sxs-lookup"><span data-stu-id="5fef9-111">Boolean</span></span>      | <span data-ttu-id="5fef9-112">Указывает, включен ли элемент управления сеансом.</span><span class="sxs-lookup"><span data-stu-id="5fef9-112">Specifies whether the session control is enabled.</span></span> |

## <a name="relationships"></a><span data-ttu-id="5fef9-113">Связи</span><span class="sxs-lookup"><span data-stu-id="5fef9-113">Relationships</span></span>

<span data-ttu-id="5fef9-114">Отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="5fef9-114">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5fef9-115">Представление в формате JSON</span><span class="sxs-lookup"><span data-stu-id="5fef9-115">JSON representation</span></span>

<span data-ttu-id="5fef9-116">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="5fef9-116">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.conditionalAccessSessionControl",
  "baseType": null
}-->

```json
{
  "isEnabled": true
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conditionalAccessSessionControl resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->