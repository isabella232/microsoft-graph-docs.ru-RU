---
title: Тип ресурса трендов
description: Отношение с широкими возможностями, соединяющее пользователя с документами, которые обрабатываются пользователем (важны для пользователя). Файлы OneDrive и файлы, хранящиеся на сайтах группы SharePoint, могут обходить пользователя.
author: simonhult
localization_priority: Normal
ms.prod: insights
doc_type: resourcePageType
ms.openlocfilehash: 624319d216758228de1c3fbed4e7b4f172a9e7ce
ms.sourcegitcommit: 1cdb3bcddf34e7445e65477b9bf661d4d10c7311
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2019
ms.locfileid: "39845002"
---
# <a name="trending-resource-type"></a><span data-ttu-id="28d30-104">Тип ресурса трендов</span><span class="sxs-lookup"><span data-stu-id="28d30-104">trending resource type</span></span>

<span data-ttu-id="28d30-105">Отношение с широкими возможностями, соединяющее пользователя с документами, которые обрабатываются пользователем (важны для пользователя).</span><span class="sxs-lookup"><span data-stu-id="28d30-105">Rich relationship connecting a user to documents that are trending around the user (are relevant to the user).</span></span> <span data-ttu-id="28d30-106">Файлы OneDrive и файлы, хранящиеся на сайтах группы SharePoint, могут обходить пользователя.</span><span class="sxs-lookup"><span data-stu-id="28d30-106">OneDrive files, and files stored on SharePoint team sites can trend around the user.</span></span>

## <a name="methods"></a><span data-ttu-id="28d30-107">Методы</span><span class="sxs-lookup"><span data-stu-id="28d30-107">Methods</span></span>

| <span data-ttu-id="28d30-108">Метод</span><span class="sxs-lookup"><span data-stu-id="28d30-108">Method</span></span>       | <span data-ttu-id="28d30-109">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="28d30-109">Return Type</span></span>  |<span data-ttu-id="28d30-110">Описание</span><span class="sxs-lookup"><span data-stu-id="28d30-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="28d30-111">Список "Популярные"</span><span class="sxs-lookup"><span data-stu-id="28d30-111">List trending</span></span>](../api/insights-list-trending.md) |<span data-ttu-id="28d30-112">Коллекция объектов [trending](insights-trending.md)</span><span class="sxs-lookup"><span data-stu-id="28d30-112">[trending](insights-trending.md) collection</span></span>| <span data-ttu-id="28d30-113">Получение списка файлов трендов.</span><span class="sxs-lookup"><span data-stu-id="28d30-113">Get a list of trending files.</span></span>|

## <a name="properties"></a><span data-ttu-id="28d30-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="28d30-114">Properties</span></span>

| <span data-ttu-id="28d30-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="28d30-115">Property</span></span>      | <span data-ttu-id="28d30-116">Тип</span><span class="sxs-lookup"><span data-stu-id="28d30-116">Type</span></span>                              | <span data-ttu-id="28d30-117">Описание</span><span class="sxs-lookup"><span data-stu-id="28d30-117">Description</span></span>  |
| ------------- |---------------                    | -------------|
| <span data-ttu-id="28d30-118">id</span><span class="sxs-lookup"><span data-stu-id="28d30-118">id</span></span>                    | <span data-ttu-id="28d30-119">String</span><span class="sxs-lookup"><span data-stu-id="28d30-119">String</span></span>                    | <span data-ttu-id="28d30-120">Уникальный идентификатор связи.</span><span class="sxs-lookup"><span data-stu-id="28d30-120">Unique identifier of the relationship.</span></span> <span data-ttu-id="28d30-121">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="28d30-121">Read only.</span></span>        |
| <span data-ttu-id="28d30-122">weight</span><span class="sxs-lookup"><span data-stu-id="28d30-122">weight</span></span>                | <span data-ttu-id="28d30-123">Двойное с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="28d30-123">Double</span></span>                    | <span data-ttu-id="28d30-124">Значение, определяющее степень тенденции документа в данный момент.</span><span class="sxs-lookup"><span data-stu-id="28d30-124">Value indicating how much the document is currently trending.</span></span> <span data-ttu-id="28d30-125">Чем больше это число, тем больше документ будет обходить пользователь (более релевантно).</span><span class="sxs-lookup"><span data-stu-id="28d30-125">The larger the number, the more the document is currently trending around the user (the more relevant it is).</span></span> <span data-ttu-id="28d30-126">Возвращенные документы сортируются по этому значению.</span><span class="sxs-lookup"><span data-stu-id="28d30-126">Returned documents are sorted by this value.</span></span>  |
| <span data-ttu-id="28d30-127">Ресурсе resourcevisualization</span><span class="sxs-lookup"><span data-stu-id="28d30-127">resourceVisualization</span></span> | [<span data-ttu-id="28d30-128">Ресурсе resourcevisualization</span><span class="sxs-lookup"><span data-stu-id="28d30-128">resourceVisualization</span></span>](insights-resourcevisualization.md)    | <span data-ttu-id="28d30-129">Свойства, которые можно использовать для отображения документа в вашем интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="28d30-129">Properties that you can use to visualize the document in your experience.</span></span> |
| <span data-ttu-id="28d30-130">ресаурцереференце</span><span class="sxs-lookup"><span data-stu-id="28d30-130">resourceReference</span></span>     | [<span data-ttu-id="28d30-131">ресаурцереференце</span><span class="sxs-lookup"><span data-stu-id="28d30-131">resourceReference</span></span>](insights-resourcereference.md)        | <span data-ttu-id="28d30-132">Справочные свойства документа тенденций, такие как URL-адрес и тип документа.</span><span class="sxs-lookup"><span data-stu-id="28d30-132">Reference properties of the trending document, such as the url and type of the document.</span></span> |
| <span data-ttu-id="28d30-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="28d30-133">lastModifiedDateTime</span></span>  | <span data-ttu-id="28d30-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="28d30-134">DateTimeOffset</span></span>            | |
## <a name="relationships"></a><span data-ttu-id="28d30-135">Связи</span><span class="sxs-lookup"><span data-stu-id="28d30-135">Relationships</span></span>

| <span data-ttu-id="28d30-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="28d30-136">Property</span></span>      | <span data-ttu-id="28d30-137">Тип</span><span class="sxs-lookup"><span data-stu-id="28d30-137">Type</span></span>          | <span data-ttu-id="28d30-138">Описание</span><span class="sxs-lookup"><span data-stu-id="28d30-138">Description</span></span>  |
| ------------- |---------------| -------------|
| <span data-ttu-id="28d30-139">resource</span><span class="sxs-lookup"><span data-stu-id="28d30-139">resource</span></span>      | <span data-ttu-id="28d30-140">.</span><span class="sxs-lookup"><span data-stu-id="28d30-140">entity</span></span>        | <span data-ttu-id="28d30-141">Используется для навигации по документу трендов.</span><span class="sxs-lookup"><span data-stu-id="28d30-141">Used for navigating to the trending document.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="28d30-142">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="28d30-142">JSON representation</span></span>

<span data-ttu-id="28d30-143">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="28d30-143">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "keyProperty":"id",
  "optionalProperties": [
    "resource"
  ],
  "@odata.type": "microsoft.graph.trending"
}-->

```json
{
  "id": "string",
  "weight": "double",
  "resourceVisualization": {"@odata.type": "microsoft.graph.resourceVisualization"},
  "resourceReference": {"@odata.type": "microsoft.graph.resourceReference"},
  "lastModifiedDateTime": "String (timestamp)"
}
```