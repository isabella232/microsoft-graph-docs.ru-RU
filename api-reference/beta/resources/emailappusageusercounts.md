---
title: Тип ресурса emailAppUsageUserCounts
description: Ниже указано представление ресурса в формате JSON.
ms.openlocfilehash: c8669c8a34987bc1e71152ae717f9be3ba101107
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27080215"
---
# <a name="emailappusageusercounts-resource-type"></a><span data-ttu-id="ecc42-103">Тип ресурса emailAppUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="ecc42-103">emailAppUsageUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="ecc42-104">Свойства</span><span class="sxs-lookup"><span data-stu-id="ecc42-104">Properties</span></span>

| <span data-ttu-id="ecc42-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="ecc42-105">Property</span></span>          | <span data-ttu-id="ecc42-106">Тип</span><span class="sxs-lookup"><span data-stu-id="ecc42-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="ecc42-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="ecc42-107">reportRefreshDate</span></span> | <span data-ttu-id="ecc42-108">Date</span><span class="sxs-lookup"><span data-stu-id="ecc42-108">Date</span></span>   |
| <span data-ttu-id="ecc42-109">mailForMac</span><span class="sxs-lookup"><span data-stu-id="ecc42-109">mailForMac</span></span>        | <span data-ttu-id="ecc42-110">Int64</span><span class="sxs-lookup"><span data-stu-id="ecc42-110">Int64</span></span>  |
| <span data-ttu-id="ecc42-111">outlookForMac</span><span class="sxs-lookup"><span data-stu-id="ecc42-111">outlookForMac</span></span>     | <span data-ttu-id="ecc42-112">Int64</span><span class="sxs-lookup"><span data-stu-id="ecc42-112">Int64</span></span>  |
| <span data-ttu-id="ecc42-113">outlookForWindows</span><span class="sxs-lookup"><span data-stu-id="ecc42-113">outlookForWindows</span></span> | <span data-ttu-id="ecc42-114">Int64</span><span class="sxs-lookup"><span data-stu-id="ecc42-114">Int64</span></span>  |
| <span data-ttu-id="ecc42-115">outlookForMobile</span><span class="sxs-lookup"><span data-stu-id="ecc42-115">outlookForMobile</span></span>  | <span data-ttu-id="ecc42-116">Int64</span><span class="sxs-lookup"><span data-stu-id="ecc42-116">Int64</span></span>  |
| <span data-ttu-id="ecc42-117">otherForMobile</span><span class="sxs-lookup"><span data-stu-id="ecc42-117">otherForMobile</span></span>    | <span data-ttu-id="ecc42-118">Int64</span><span class="sxs-lookup"><span data-stu-id="ecc42-118">Int64</span></span>  |
| <span data-ttu-id="ecc42-119">outlookForWeb</span><span class="sxs-lookup"><span data-stu-id="ecc42-119">outlookForWeb</span></span>     | <span data-ttu-id="ecc42-120">Int64</span><span class="sxs-lookup"><span data-stu-id="ecc42-120">Int64</span></span>  |
| <span data-ttu-id="ecc42-121">pop3App</span><span class="sxs-lookup"><span data-stu-id="ecc42-121">pop3App</span></span>           | <span data-ttu-id="ecc42-122">Int64</span><span class="sxs-lookup"><span data-stu-id="ecc42-122">Int64</span></span>  |
| <span data-ttu-id="ecc42-123">imap4App</span><span class="sxs-lookup"><span data-stu-id="ecc42-123">imap4App</span></span>          | <span data-ttu-id="ecc42-124">Int64</span><span class="sxs-lookup"><span data-stu-id="ecc42-124">Int64</span></span>  |
| <span data-ttu-id="ecc42-125">smtpApp</span><span class="sxs-lookup"><span data-stu-id="ecc42-125">smtpApp</span></span>           | <span data-ttu-id="ecc42-126">Int64</span><span class="sxs-lookup"><span data-stu-id="ecc42-126">Int64</span></span>  |
| <span data-ttu-id="ecc42-127">reportDate</span><span class="sxs-lookup"><span data-stu-id="ecc42-127">reportDate</span></span>        | <span data-ttu-id="ecc42-128">Date</span><span class="sxs-lookup"><span data-stu-id="ecc42-128">Date</span></span>   |
| <span data-ttu-id="ecc42-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="ecc42-129">reportPeriod</span></span>      | <span data-ttu-id="ecc42-130">String</span><span class="sxs-lookup"><span data-stu-id="ecc42-130">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ecc42-131">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="ecc42-131">JSON representation</span></span>

<span data-ttu-id="ecc42-132">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="ecc42-132">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.emailAppUsageUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "mailForMac": 1024, 
  "outlookForMac": 1024, 
  "outlookForWindows": 1024, 
  "outlookForMobile": 1024, 
  "otherForMobile": 1024, 
  "outlookForWeb": 1024, 
  "pop3App": 1024, 
  "imap4App": 1024, 
  "smtpApp": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
