---
title: Тип ресурса Phone
description: Представляет номер телефона.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: ''
author: davidmu1
ms.openlocfilehash: 0e87557a3c31ef1fb8f5ebbbdd2ff29b67d8ff8c
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47997909"
---
# <a name="phone-resource-type"></a><span data-ttu-id="62efc-103">Тип ресурса Phone</span><span class="sxs-lookup"><span data-stu-id="62efc-103">phone resource type</span></span>

<span data-ttu-id="62efc-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="62efc-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="62efc-105">Представляет номер телефона.</span><span class="sxs-lookup"><span data-stu-id="62efc-105">Represents a phone number.</span></span>


## <a name="properties"></a><span data-ttu-id="62efc-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="62efc-106">Properties</span></span>
| <span data-ttu-id="62efc-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="62efc-107">Property</span></span>     | <span data-ttu-id="62efc-108">Тип</span><span class="sxs-lookup"><span data-stu-id="62efc-108">Type</span></span>   |<span data-ttu-id="62efc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="62efc-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="62efc-110">число</span><span class="sxs-lookup"><span data-stu-id="62efc-110">number</span></span>|<span data-ttu-id="62efc-111">string</span><span class="sxs-lookup"><span data-stu-id="62efc-111">string</span></span>|<span data-ttu-id="62efc-112">Номер телефона.</span><span class="sxs-lookup"><span data-stu-id="62efc-112">The phone number.</span></span>|
|<span data-ttu-id="62efc-113">type</span><span class="sxs-lookup"><span data-stu-id="62efc-113">type</span></span>|<span data-ttu-id="62efc-114">String</span><span class="sxs-lookup"><span data-stu-id="62efc-114">String</span></span>|<span data-ttu-id="62efc-115">Тип номера телефона.</span><span class="sxs-lookup"><span data-stu-id="62efc-115">The type of phone number.</span></span> <span data-ttu-id="62efc-116">Возможные значения: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span><span class="sxs-lookup"><span data-stu-id="62efc-116">Possible values are: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="62efc-117">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="62efc-117">JSON representation</span></span>

<span data-ttu-id="62efc-118">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="62efc-118">Here is a JSON representation of the resource.</span></span>

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


