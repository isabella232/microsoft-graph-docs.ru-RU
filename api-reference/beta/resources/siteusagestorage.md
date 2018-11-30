---
title: Тип ресурса siteUsageStorage
description: Ниже указано представление ресурса в формате JSON.
ms.openlocfilehash: 1fdfa6cb2690d6dbacf5e534792061b6e64025d8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27076054"
---
# <a name="siteusagestorage-resource-type"></a><span data-ttu-id="a53fb-103">Тип ресурса siteUsageStorage</span><span class="sxs-lookup"><span data-stu-id="a53fb-103">siteUsageStorage resource type</span></span>

## <a name="properties"></a><span data-ttu-id="a53fb-104">Свойства</span><span class="sxs-lookup"><span data-stu-id="a53fb-104">Properties</span></span>

| <span data-ttu-id="a53fb-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="a53fb-105">Property</span></span>           | <span data-ttu-id="a53fb-106">Тип</span><span class="sxs-lookup"><span data-stu-id="a53fb-106">Type</span></span>   |
| :----------------- | :----- |
| <span data-ttu-id="a53fb-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="a53fb-107">reportRefreshDate</span></span>  | <span data-ttu-id="a53fb-108">Date</span><span class="sxs-lookup"><span data-stu-id="a53fb-108">Date</span></span>   |
| <span data-ttu-id="a53fb-109">siteType</span><span class="sxs-lookup"><span data-stu-id="a53fb-109">siteType</span></span>           | <span data-ttu-id="a53fb-110">String</span><span class="sxs-lookup"><span data-stu-id="a53fb-110">String</span></span> |
| <span data-ttu-id="a53fb-111">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="a53fb-111">storageUsedInBytes</span></span> | <span data-ttu-id="a53fb-112">Int64</span><span class="sxs-lookup"><span data-stu-id="a53fb-112">Int64</span></span>  |
| <span data-ttu-id="a53fb-113">reportDate</span><span class="sxs-lookup"><span data-stu-id="a53fb-113">reportDate</span></span>         | <span data-ttu-id="a53fb-114">Date</span><span class="sxs-lookup"><span data-stu-id="a53fb-114">Date</span></span>   |
| <span data-ttu-id="a53fb-115">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="a53fb-115">reportPeriod</span></span>       | <span data-ttu-id="a53fb-116">String</span><span class="sxs-lookup"><span data-stu-id="a53fb-116">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a53fb-117">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="a53fb-117">JSON representation</span></span>

<span data-ttu-id="a53fb-118">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="a53fb-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.siteUsageStorage"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "siteType": "String", 
  "storageUsedInBytes": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
