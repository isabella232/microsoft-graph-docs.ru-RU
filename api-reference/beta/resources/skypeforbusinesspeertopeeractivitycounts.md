---
title: Тип ресурса skypeForBusinessPeerToPeerActivityCounts
description: Ниже указано представление ресурса в формате JSON.
localization_priority: Normal
ms.openlocfilehash: 4baf218ed9398a8f208c4d1d44a28579773dea6f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874475"
---
# <a name="skypeforbusinesspeertopeeractivitycounts-resource-type"></a><span data-ttu-id="f3c1e-103">Тип ресурса skypeForBusinessPeerToPeerActivityCounts</span><span class="sxs-lookup"><span data-stu-id="f3c1e-103">skypeForBusinessPeerToPeerActivityCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="f3c1e-104">Свойства</span><span class="sxs-lookup"><span data-stu-id="f3c1e-104">Properties</span></span>

| <span data-ttu-id="f3c1e-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="f3c1e-105">Property</span></span>          | <span data-ttu-id="f3c1e-106">Тип</span><span class="sxs-lookup"><span data-stu-id="f3c1e-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="f3c1e-107">обмен мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="f3c1e-107">im</span></span>                | <span data-ttu-id="f3c1e-108">Int64</span><span class="sxs-lookup"><span data-stu-id="f3c1e-108">Int64</span></span>  |
| <span data-ttu-id="f3c1e-109">audio</span><span class="sxs-lookup"><span data-stu-id="f3c1e-109">audio</span></span>             | <span data-ttu-id="f3c1e-110">Int64</span><span class="sxs-lookup"><span data-stu-id="f3c1e-110">Int64</span></span>  |
| <span data-ttu-id="f3c1e-111">video</span><span class="sxs-lookup"><span data-stu-id="f3c1e-111">video</span></span>             | <span data-ttu-id="f3c1e-112">Int64</span><span class="sxs-lookup"><span data-stu-id="f3c1e-112">Int64</span></span>  |
| <span data-ttu-id="f3c1e-113">appSharing</span><span class="sxs-lookup"><span data-stu-id="f3c1e-113">appSharing</span></span>        | <span data-ttu-id="f3c1e-114">Int64</span><span class="sxs-lookup"><span data-stu-id="f3c1e-114">Int64</span></span>  |
| <span data-ttu-id="f3c1e-115">fileTransfer</span><span class="sxs-lookup"><span data-stu-id="f3c1e-115">fileTransfer</span></span>      | <span data-ttu-id="f3c1e-116">Int64</span><span class="sxs-lookup"><span data-stu-id="f3c1e-116">Int64</span></span>  |
| <span data-ttu-id="f3c1e-117">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="f3c1e-117">reportRefreshDate</span></span> | <span data-ttu-id="f3c1e-118">Date</span><span class="sxs-lookup"><span data-stu-id="f3c1e-118">Date</span></span>   |
| <span data-ttu-id="f3c1e-119">reportDate</span><span class="sxs-lookup"><span data-stu-id="f3c1e-119">reportDate</span></span>        | <span data-ttu-id="f3c1e-120">Date</span><span class="sxs-lookup"><span data-stu-id="f3c1e-120">Date</span></span>   |
| <span data-ttu-id="f3c1e-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="f3c1e-121">reportPeriod</span></span>      | <span data-ttu-id="f3c1e-122">String</span><span class="sxs-lookup"><span data-stu-id="f3c1e-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="f3c1e-123">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="f3c1e-123">JSON representation</span></span>

<span data-ttu-id="f3c1e-124">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="f3c1e-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessPeerToPeerActivityCounts"
} -->

```json
{
  "im": 1024, 
  "audio": 1024, 
  "video": 1024, 
  "appSharing": 1024, 
  "fileTransfer": 1024, 
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
