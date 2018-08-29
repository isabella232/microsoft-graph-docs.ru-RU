---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: calculatedColumn
ms.openlocfilehash: 7e26b3683c2c84d1c413f3214da39e0a3d016f40
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267845"
---
# <a name="calculatedcolumn-resource-type"></a><span data-ttu-id="ce04b-102">Тип ресурса calculatedColumn</span><span class="sxs-lookup"><span data-stu-id="ce04b-102">CalculatedColumn resource type</span></span>

<span data-ttu-id="ce04b-103">Ресурс **calculatedColumn** в ресурсе [columnDefinition](columnDefinition.md) указывает, что данные столбца вычисляются на основании значений в других столбцах на сайте.</span><span class="sxs-lookup"><span data-stu-id="ce04b-103">The **calculatedColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's data is calculated based on other columns in the site.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ce04b-104">Представление в формате JSON</span><span class="sxs-lookup"><span data-stu-id="ce04b-104">JSON representation</span></span>

<span data-ttu-id="ce04b-105">Ниже показано представление ресурса **calculatedColumn** в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="ce04b-105">Here is a JSON representation of a **calculatedColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.calculatedColumn" } -->

```json
{
  "format": "dateOnly | dateTime",
  "formula": "=[Column1]+[Column2]+[Column3]",
  "outputType": "boolean | currency | dateTime | number | text",
}
```

## <a name="properties"></a><span data-ttu-id="ce04b-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="ce04b-106">Properties</span></span>

| <span data-ttu-id="ce04b-107">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="ce04b-107">Property name</span></span>  | <span data-ttu-id="ce04b-108">Тип</span><span class="sxs-lookup"><span data-stu-id="ce04b-108">Type</span></span>    | <span data-ttu-id="ce04b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ce04b-109">Description</span></span>
|:---------------|:--------|:--------------------------------------------------
| <span data-ttu-id="ce04b-110">**format**</span><span class="sxs-lookup"><span data-stu-id="ce04b-110">**format**</span></span>     | <span data-ttu-id="ce04b-111">строка</span><span class="sxs-lookup"><span data-stu-id="ce04b-111">string</span></span>  | <span data-ttu-id="ce04b-112">Для типов выходных данных `dateTime` это свойство указывает формат значения.</span><span class="sxs-lookup"><span data-stu-id="ce04b-112">For `dateTime` output types, the format of the value.</span></span> <span data-ttu-id="ce04b-113">Должно иметь тип `dateOnly` или `dateTime`.</span><span class="sxs-lookup"><span data-stu-id="ce04b-113">Must be one of `dateOnly` or `dateTime`.</span></span>
| <span data-ttu-id="ce04b-114">**formula**</span><span class="sxs-lookup"><span data-stu-id="ce04b-114">**formula**</span></span>    | <span data-ttu-id="ce04b-115">строка</span><span class="sxs-lookup"><span data-stu-id="ce04b-115">string</span></span>  | <span data-ttu-id="ce04b-116">Формула, используемая для вычисления значения для данного столбца.</span><span class="sxs-lookup"><span data-stu-id="ce04b-116">The formula used to compute the value for this column.</span></span>
| <span data-ttu-id="ce04b-117">**outputType**</span><span class="sxs-lookup"><span data-stu-id="ce04b-117">**outputType**</span></span> | <span data-ttu-id="ce04b-118">строка</span><span class="sxs-lookup"><span data-stu-id="ce04b-118">string</span></span>  | <span data-ttu-id="ce04b-119">Тип выходных данных, используемый для форматирования значений в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="ce04b-119">The output type used to format values in this column.</span></span> <span data-ttu-id="ce04b-120">Должно иметь один из типов `boolean`, `currency`, `dateTime`, `number` или `text`.</span><span class="sxs-lookup"><span data-stu-id="ce04b-120">Must be one of `boolean`, `currency`, `dateTime`, `number`, or `text`.</span></span>

<span data-ttu-id="ce04b-121">В формулах SharePoint используется синтаксис, похожий на синтаксис формул в Excel.</span><span class="sxs-lookup"><span data-stu-id="ce04b-121">SharePoint formulas use a syntax similar to Excel formulas.</span></span>
<span data-ttu-id="ce04b-122">Дополнительные сведения см. в статье [Примеры часто используемых формул в списках SharePoint][SPFormulas].</span><span class="sxs-lookup"><span data-stu-id="ce04b-122">See [Examples of common formulas in SharePoint Lists][SPFormulas] for more information.</span></span>

[SPFormulas]: https://support.office.com/en-us/article/Examples-of-common-formulas-in-SharePoint-Lists-d81f5f21-2b4e-45ce-b170-bf7ebf6988b3

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/calculatedcolumn.md:
      Found potential enums in resource example that weren't defined in a table:(dateOnly,dateTime) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/calculatedcolumn.md:
      Found potential enums in resource example that weren't defined in a table:(boolean,currency,dateTime,number,text) are in resource, but () are in table"
  ],
  "tocPath": "Resources/CalculatedColumn"
} -->
