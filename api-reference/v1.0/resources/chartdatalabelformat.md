---
title: Тип ресурса ChartDataLabelFormat
description: Инкапсулирует свойства формата для меток данных диаграммы.
ms.openlocfilehash: ec81523dc09c17cd8c7fb9d543c2214377201260
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27025402"
---
# <a name="chartdatalabelformat-resource-type"></a><span data-ttu-id="b831d-103">Тип ресурса ChartDataLabelFormat</span><span class="sxs-lookup"><span data-stu-id="b831d-103">ChartDataLabelFormat resource type</span></span>

<span data-ttu-id="b831d-104">Инкапсулирует свойства формата для меток данных диаграммы.</span><span class="sxs-lookup"><span data-stu-id="b831d-104">Encapsulates the format properties for the chart data labels.</span></span>


## <a name="methods"></a><span data-ttu-id="b831d-105">Методы</span><span class="sxs-lookup"><span data-stu-id="b831d-105">Methods</span></span>
<span data-ttu-id="b831d-106">Нет</span><span class="sxs-lookup"><span data-stu-id="b831d-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="b831d-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="b831d-107">Properties</span></span>
<span data-ttu-id="b831d-108">Нет</span><span class="sxs-lookup"><span data-stu-id="b831d-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="b831d-109">Связи</span><span class="sxs-lookup"><span data-stu-id="b831d-109">Relationships</span></span>
| <span data-ttu-id="b831d-110">Связь</span><span class="sxs-lookup"><span data-stu-id="b831d-110">Relationship</span></span> | <span data-ttu-id="b831d-111">Тип</span><span class="sxs-lookup"><span data-stu-id="b831d-111">Type</span></span>   |<span data-ttu-id="b831d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b831d-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b831d-113">fill</span><span class="sxs-lookup"><span data-stu-id="b831d-113">fill</span></span>|[<span data-ttu-id="b831d-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="b831d-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="b831d-p101">Представляет формат заливки для текущей метки данных диаграммы. Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b831d-p101">Represents the fill format of the current chart data label. Read-only.</span></span>|
|<span data-ttu-id="b831d-117">font</span><span class="sxs-lookup"><span data-stu-id="b831d-117">font</span></span>|[<span data-ttu-id="b831d-118">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="b831d-118">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="b831d-p102">Представляет атрибуты шрифта (имя, размер, цвет и т. д.) для метки данных диаграммы. Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b831d-p102">Represents the font attributes (font name, font size, color, etc.) for a chart data label. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="b831d-121">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="b831d-121">JSON representation</span></span>

<span data-ttu-id="b831d-122">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="b831d-122">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartDataLabelFormat"
}-->

```json
{
  "fill": {"@odata.type": "microsoft.graph.workbookChartFill"},
  "font": {"@odata.type": "microsoft.graph.workbookChartFont"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartDataLabelFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->