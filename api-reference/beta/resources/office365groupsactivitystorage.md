---
title: Тип ресурса office365GroupsActivityStorage
description: Ниже указано представление ресурса в формате JSON.
localization_priority: Normal
ms.openlocfilehash: 9824d3d172a8578f8a25a049c2d0d3b407bbc47e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862253"
---
# <a name="office365groupsactivitystorage-resource-type"></a><span data-ttu-id="3ed5b-103">Тип ресурса office365GroupsActivityStorage</span><span class="sxs-lookup"><span data-stu-id="3ed5b-103">office365GroupsActivityStorage resource type</span></span>

## <a name="properties"></a><span data-ttu-id="3ed5b-104">Свойства</span><span class="sxs-lookup"><span data-stu-id="3ed5b-104">Properties</span></span>

| <span data-ttu-id="3ed5b-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="3ed5b-105">Property</span></span>                  | <span data-ttu-id="3ed5b-106">Тип</span><span class="sxs-lookup"><span data-stu-id="3ed5b-106">Type</span></span>   | <span data-ttu-id="3ed5b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3ed5b-107">Description</span></span>                              |
| :------------------------ | :----- | ---------------------------------------- |
| <span data-ttu-id="3ed5b-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="3ed5b-108">reportRefreshDate</span></span>         | <span data-ttu-id="3ed5b-109">Date</span><span class="sxs-lookup"><span data-stu-id="3ed5b-109">Date</span></span>   | <span data-ttu-id="3ed5b-110">Последняя дата контента.</span><span class="sxs-lookup"><span data-stu-id="3ed5b-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="3ed5b-111">mailboxStorageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="3ed5b-111">mailboxStorageUsedInBytes</span></span> | <span data-ttu-id="3ed5b-112">Int64</span><span class="sxs-lookup"><span data-stu-id="3ed5b-112">Int64</span></span>  | <span data-ttu-id="3ed5b-113">Используются в почтовом ящике группы хранения.</span><span class="sxs-lookup"><span data-stu-id="3ed5b-113">The storage used in group mailbox.</span></span>       |
| <span data-ttu-id="3ed5b-114">siteStorageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="3ed5b-114">siteStorageUsedInBytes</span></span>    | <span data-ttu-id="3ed5b-115">Int64</span><span class="sxs-lookup"><span data-stu-id="3ed5b-115">Int64</span></span>  | <span data-ttu-id="3ed5b-116">Хранения, используемый в библиотеке документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3ed5b-116">The storage used in SharePoint document library.</span></span> |
| <span data-ttu-id="3ed5b-117">reportDate</span><span class="sxs-lookup"><span data-stu-id="3ed5b-117">reportDate</span></span>                | <span data-ttu-id="3ed5b-118">Date</span><span class="sxs-lookup"><span data-stu-id="3ed5b-118">Date</span></span>   | <span data-ttu-id="3ed5b-119">Дата моментальный снимок для Exchange и SharePoint используется хранилища.</span><span class="sxs-lookup"><span data-stu-id="3ed5b-119">The snapshot date for Exchange and SharePoint used storage.</span></span> |
| <span data-ttu-id="3ed5b-120">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="3ed5b-120">reportPeriod</span></span>              | <span data-ttu-id="3ed5b-121">Строка</span><span class="sxs-lookup"><span data-stu-id="3ed5b-121">String</span></span> | <span data-ttu-id="3ed5b-122">Количество дней, на которое отчета.</span><span class="sxs-lookup"><span data-stu-id="3ed5b-122">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="3ed5b-123">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="3ed5b-123">JSON representation</span></span>

<span data-ttu-id="3ed5b-124">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="3ed5b-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365GroupsActivityStorage"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "mailboxStorageUsedInBytes": 1024, 
  "siteStorageUsedInBytes": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
