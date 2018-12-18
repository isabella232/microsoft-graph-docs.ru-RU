---
title: Тип ресурса teamsDeviceUsageUserCounts
description: Ниже указано представление ресурса в формате JSON.
author: nkramer
ms.openlocfilehash: 1255a8e1e92bb461d5c100c72e9030f57db5f8fa
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306512"
---
# <a name="teamsdeviceusageusercounts-resource-type"></a><span data-ttu-id="64065-103">Тип ресурса teamsDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="64065-103">teamsDeviceUsageUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="64065-104">Свойства</span><span class="sxs-lookup"><span data-stu-id="64065-104">Properties</span></span>

| <span data-ttu-id="64065-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="64065-105">Property</span></span>          | <span data-ttu-id="64065-106">Тип</span><span class="sxs-lookup"><span data-stu-id="64065-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="64065-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="64065-107">reportRefreshDate</span></span> | <span data-ttu-id="64065-108">Date</span><span class="sxs-lookup"><span data-stu-id="64065-108">Date</span></span>   |
| <span data-ttu-id="64065-109">web</span><span class="sxs-lookup"><span data-stu-id="64065-109">web</span></span>               | <span data-ttu-id="64065-110">Int64</span><span class="sxs-lookup"><span data-stu-id="64065-110">Int64</span></span>  |
| <span data-ttu-id="64065-111">windowsPhone</span><span class="sxs-lookup"><span data-stu-id="64065-111">windowsPhone</span></span>      | <span data-ttu-id="64065-112">Int64</span><span class="sxs-lookup"><span data-stu-id="64065-112">Int64</span></span>  |
| <span data-ttu-id="64065-113">androidPhone</span><span class="sxs-lookup"><span data-stu-id="64065-113">androidPhone</span></span>      | <span data-ttu-id="64065-114">Int64</span><span class="sxs-lookup"><span data-stu-id="64065-114">Int64</span></span>  |
| <span data-ttu-id="64065-115">операций ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="64065-115">ios</span></span>               | <span data-ttu-id="64065-116">Int64</span><span class="sxs-lookup"><span data-stu-id="64065-116">Int64</span></span>  |
| <span data-ttu-id="64065-117">mac</span><span class="sxs-lookup"><span data-stu-id="64065-117">mac</span></span>               | <span data-ttu-id="64065-118">Int64</span><span class="sxs-lookup"><span data-stu-id="64065-118">Int64</span></span>  |
| <span data-ttu-id="64065-119">Windows</span><span class="sxs-lookup"><span data-stu-id="64065-119">windows</span></span>           | <span data-ttu-id="64065-120">Int64</span><span class="sxs-lookup"><span data-stu-id="64065-120">Int64</span></span>  |
| <span data-ttu-id="64065-121">reportDate</span><span class="sxs-lookup"><span data-stu-id="64065-121">reportDate</span></span>        | <span data-ttu-id="64065-122">Date</span><span class="sxs-lookup"><span data-stu-id="64065-122">Date</span></span>   |
| <span data-ttu-id="64065-123">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="64065-123">reportPeriod</span></span>      | <span data-ttu-id="64065-124">String</span><span class="sxs-lookup"><span data-stu-id="64065-124">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="64065-125">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="64065-125">JSON representation</span></span>

<span data-ttu-id="64065-126">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="64065-126">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsDeviceUsageUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "web": 1024, 
  "windowsPhone": 1024, 
  "androidPhone": 1024, 
  "ios": 1024, 
  "mac": 1024, 
  "windows": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
