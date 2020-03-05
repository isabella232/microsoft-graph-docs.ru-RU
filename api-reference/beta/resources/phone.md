---
title: Тип ресурса Phone
description: Представляет номер телефона.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: ''
author: ''
ms.openlocfilehash: ca2c81531aa5bf53c8038fe7e095f056c4682eba
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42521892"
---
# <a name="phone-resource-type"></a><span data-ttu-id="b8c31-103">Тип ресурса Phone</span><span class="sxs-lookup"><span data-stu-id="b8c31-103">phone resource type</span></span>

<span data-ttu-id="b8c31-104">Пространство имен: Microsoft. Graph</span><span class="sxs-lookup"><span data-stu-id="b8c31-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="b8c31-105">Представляет номер телефона.</span><span class="sxs-lookup"><span data-stu-id="b8c31-105">Represents a phone number.</span></span>


## <a name="properties"></a><span data-ttu-id="b8c31-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="b8c31-106">Properties</span></span>
| <span data-ttu-id="b8c31-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="b8c31-107">Property</span></span>     | <span data-ttu-id="b8c31-108">Тип</span><span class="sxs-lookup"><span data-stu-id="b8c31-108">Type</span></span>   |<span data-ttu-id="b8c31-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b8c31-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b8c31-110">число</span><span class="sxs-lookup"><span data-stu-id="b8c31-110">number</span></span>|<span data-ttu-id="b8c31-111">строка</span><span class="sxs-lookup"><span data-stu-id="b8c31-111">string</span></span>|<span data-ttu-id="b8c31-112">Номер телефона.</span><span class="sxs-lookup"><span data-stu-id="b8c31-112">The phone number.</span></span>|
|<span data-ttu-id="b8c31-113">type</span><span class="sxs-lookup"><span data-stu-id="b8c31-113">type</span></span>|<span data-ttu-id="b8c31-114">String</span><span class="sxs-lookup"><span data-stu-id="b8c31-114">String</span></span>|<span data-ttu-id="b8c31-115">Тип номера телефона.</span><span class="sxs-lookup"><span data-stu-id="b8c31-115">The type of phone number.</span></span> <span data-ttu-id="b8c31-116">Возможные значения: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span><span class="sxs-lookup"><span data-stu-id="b8c31-116">Possible values are: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b8c31-117">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="b8c31-117">JSON representation</span></span>

<span data-ttu-id="b8c31-118">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="b8c31-118">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.phone"
}-->

```json
{
  "number": "string",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "phone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
