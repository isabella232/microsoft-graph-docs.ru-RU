---
title: Тип ресурса Едукатионформресаурце
description: Подкласс объекта Едукатионресаурце. Этот ресурс является формой.
author: mmast-msft
localization_priority: Normal
ms.prod: education
doc_type: resourcePageType
ms.openlocfilehash: ed81e1e9e74ad311e4102963649ff4a4015bb093
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42501964"
---
# <a name="educationformresource-resource-type"></a><span data-ttu-id="cea53-104">Тип ресурса Едукатионформресаурце</span><span class="sxs-lookup"><span data-stu-id="cea53-104">educationFormResource resource type</span></span>

<span data-ttu-id="cea53-105">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="cea53-105">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="cea53-106">Подкласс объекта [едукатионресаурце](educationresource.md).</span><span class="sxs-lookup"><span data-stu-id="cea53-106">A subclass of [educationResource](educationresource.md).</span></span> <span data-ttu-id="cea53-107">Этот ресурс является формой.</span><span class="sxs-lookup"><span data-stu-id="cea53-107">This resource is a form.</span></span>


## <a name="properties"></a><span data-ttu-id="cea53-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="cea53-108">Properties</span></span>
| <span data-ttu-id="cea53-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="cea53-109">Property</span></span>     | <span data-ttu-id="cea53-110">Тип</span><span class="sxs-lookup"><span data-stu-id="cea53-110">Type</span></span>   |<span data-ttu-id="cea53-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cea53-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cea53-112">оригиналформид</span><span class="sxs-lookup"><span data-stu-id="cea53-112">originalFormId</span></span>|<span data-ttu-id="cea53-113">String</span><span class="sxs-lookup"><span data-stu-id="cea53-113">String</span></span>|<span data-ttu-id="cea53-114">Исходный идентификатор формы.</span><span class="sxs-lookup"><span data-stu-id="cea53-114">Original id of the Form.</span></span>|
|<span data-ttu-id="cea53-115">формид</span><span class="sxs-lookup"><span data-stu-id="cea53-115">formId</span></span>|<span data-ttu-id="cea53-116">String</span><span class="sxs-lookup"><span data-stu-id="cea53-116">String</span></span>|<span data-ttu-id="cea53-117">Идентификатор формы.</span><span class="sxs-lookup"><span data-stu-id="cea53-117">Id of the Form.</span></span>|
|<span data-ttu-id="cea53-118">исграупформ</span><span class="sxs-lookup"><span data-stu-id="cea53-118">isGroupForm</span></span>|<span data-ttu-id="cea53-119">Boolean</span><span class="sxs-lookup"><span data-stu-id="cea53-119">Boolean</span></span>|<span data-ttu-id="cea53-120">Принадлежность формы группе классов.</span><span class="sxs-lookup"><span data-stu-id="cea53-120">Whether the Form belongs to a class group.</span></span>|
|<span data-ttu-id="cea53-121">виевурл</span><span class="sxs-lookup"><span data-stu-id="cea53-121">viewUrl</span></span>|<span data-ttu-id="cea53-122">String</span><span class="sxs-lookup"><span data-stu-id="cea53-122">String</span></span>|<span data-ttu-id="cea53-123">URL-адрес студента для формы.</span><span class="sxs-lookup"><span data-stu-id="cea53-123">Student URL for the Form.</span></span>|
|<span data-ttu-id="cea53-124">виевурл</span><span class="sxs-lookup"><span data-stu-id="cea53-124">viewUrl</span></span>|<span data-ttu-id="cea53-125">String</span><span class="sxs-lookup"><span data-stu-id="cea53-125">String</span></span>|<span data-ttu-id="cea53-126">URL-адрес студента для формы.</span><span class="sxs-lookup"><span data-stu-id="cea53-126">Student URL for the Form.</span></span>|
|<span data-ttu-id="cea53-127">едитурл</span><span class="sxs-lookup"><span data-stu-id="cea53-127">editUrl</span></span>|<span data-ttu-id="cea53-128">String</span><span class="sxs-lookup"><span data-stu-id="cea53-128">String</span></span>|<span data-ttu-id="cea53-129">URL-адрес преподавателя для формы.</span><span class="sxs-lookup"><span data-stu-id="cea53-129">Teacher URL for the Form.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="cea53-130">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="cea53-130">JSON representation</span></span>

<span data-ttu-id="cea53-131">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="cea53-131">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationFormResource"
}-->

```json
{
  "originalFormId": "String",
  "formId": "String",
  "isGroupForm": "Boolean",
  "viewUrl": "String",
  "editUrl": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "educationFormResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
