---
title: Тип ресурса ChartGridlines
description: Представляет основные или вспомогательные линии сетки на оси диаграммы.
ms.openlocfilehash: c09580b2c669710d8aabf60e31c3c36965bfaa6a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27074854"
---
# <a name="chartgridlines-resource-type"></a><span data-ttu-id="e93ae-103">Тип ресурса ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="e93ae-103">ChartGridlines resource type</span></span>

> <span data-ttu-id="e93ae-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="e93ae-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e93ae-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e93ae-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e93ae-106">Представляет основные или вспомогательные линии сетки на оси диаграммы.</span><span class="sxs-lookup"><span data-stu-id="e93ae-106">Represents major or minor gridlines on a chart axis.</span></span>


## <a name="methods"></a><span data-ttu-id="e93ae-107">Методы</span><span class="sxs-lookup"><span data-stu-id="e93ae-107">Methods</span></span>

| <span data-ttu-id="e93ae-108">Метод</span><span class="sxs-lookup"><span data-stu-id="e93ae-108">Method</span></span>           | <span data-ttu-id="e93ae-109">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="e93ae-109">Return Type</span></span>    |<span data-ttu-id="e93ae-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e93ae-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e93ae-111">Получение объекта ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="e93ae-111">Get ChartGridlines</span></span>](../api/chartgridlines-get.md) | [<span data-ttu-id="e93ae-112">ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="e93ae-112">ChartGridlines</span></span>](chartgridlines.md) |<span data-ttu-id="e93ae-113">Чтение свойств и связей объекта chartGridlines.</span><span class="sxs-lookup"><span data-stu-id="e93ae-113">Read properties and relationships of chartGridlines object.</span></span>|
|[<span data-ttu-id="e93ae-114">Update</span><span class="sxs-lookup"><span data-stu-id="e93ae-114">Update</span></span>](../api/chartgridlines-update.md) | [<span data-ttu-id="e93ae-115">ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="e93ae-115">ChartGridlines</span></span>](chartgridlines.md)    |<span data-ttu-id="e93ae-116">Обновление объекта ChartGridlines.</span><span class="sxs-lookup"><span data-stu-id="e93ae-116">Update ChartGridlines object.</span></span> |

## <a name="properties"></a><span data-ttu-id="e93ae-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="e93ae-117">Properties</span></span>
| <span data-ttu-id="e93ae-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="e93ae-118">Property</span></span>     | <span data-ttu-id="e93ae-119">Тип</span><span class="sxs-lookup"><span data-stu-id="e93ae-119">Type</span></span>   |<span data-ttu-id="e93ae-120">Описание</span><span class="sxs-lookup"><span data-stu-id="e93ae-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e93ae-121">visible</span><span class="sxs-lookup"><span data-stu-id="e93ae-121">visible</span></span>|<span data-ttu-id="e93ae-122">boolean</span><span class="sxs-lookup"><span data-stu-id="e93ae-122">boolean</span></span>|<span data-ttu-id="e93ae-123">Логическое значение, определяющее, отображаются ли линии сетки оси.</span><span class="sxs-lookup"><span data-stu-id="e93ae-123">Boolean value representing if the axis gridlines are visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e93ae-124">Связи</span><span class="sxs-lookup"><span data-stu-id="e93ae-124">Relationships</span></span>
| <span data-ttu-id="e93ae-125">Связь</span><span class="sxs-lookup"><span data-stu-id="e93ae-125">Relationship</span></span> | <span data-ttu-id="e93ae-126">Тип</span><span class="sxs-lookup"><span data-stu-id="e93ae-126">Type</span></span>   |<span data-ttu-id="e93ae-127">Описание</span><span class="sxs-lookup"><span data-stu-id="e93ae-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e93ae-128">format</span><span class="sxs-lookup"><span data-stu-id="e93ae-128">format</span></span>|[<span data-ttu-id="e93ae-129">ChartGridlinesFormat</span><span class="sxs-lookup"><span data-stu-id="e93ae-129">ChartGridlinesFormat</span></span>](chartgridlinesformat.md)|<span data-ttu-id="e93ae-p102">Представляет форматирование линий сетки диаграммы. Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e93ae-p102">Represents the formatting of chart gridlines. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e93ae-132">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="e93ae-132">JSON representation</span></span>

<span data-ttu-id="e93ae-133">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="e93ae-133">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartGridLines"
}-->

```json
{
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartGridlines resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->