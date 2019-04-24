---
title: Тип ресурса Теамстабконфигуратион (Open Type)
description: Параметры, определяющие содержимое вкладки.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 9873d9e03fec5d7751270b963015aed9eeb0ab48
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32456983"
---
# <a name="teamstabconfiguration-resource-type-open-type"></a><span data-ttu-id="0aaa6-103">Тип ресурса Теамстабконфигуратион (Open Type)</span><span class="sxs-lookup"><span data-stu-id="0aaa6-103">teamsTabConfiguration resource type (Open Type)</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="0aaa6-104">Параметры, определяющие содержимое [вкладки](teamstab.md). При настройке вкладки в интерактивном режиме эти сведения задаются приложением поставщика вкладок.</span><span class="sxs-lookup"><span data-stu-id="0aaa6-104">The settings that determine the content of a [tab](teamstab.md). When a tab is interactively configured, this information is set by the tab provider application.</span></span>
<span data-ttu-id="0aaa6-105">Помимо приведенных ниже свойств, некоторые приложения поставщика вкладок задают дополнительные настраиваемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0aaa6-105">In addition to the properties below, some tab provider applications specify additional custom properties.</span></span>

## <a name="properties"></a><span data-ttu-id="0aaa6-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="0aaa6-106">Properties</span></span>

|<span data-ttu-id="0aaa6-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="0aaa6-107">Property</span></span>|<span data-ttu-id="0aaa6-108">Тип</span><span class="sxs-lookup"><span data-stu-id="0aaa6-108">Type</span></span>|<span data-ttu-id="0aaa6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0aaa6-109">Description</span></span>|
|-|-|-|
|  <span data-ttu-id="0aaa6-110">entityId</span><span class="sxs-lookup"><span data-stu-id="0aaa6-110">entityId</span></span>   |   <span data-ttu-id="0aaa6-111">строка</span><span class="sxs-lookup"><span data-stu-id="0aaa6-111">string</span></span> |  <span data-ttu-id="0aaa6-112">Идентификатор для сущности, размещенной у поставщика вкладок.</span><span class="sxs-lookup"><span data-stu-id="0aaa6-112">Identifier for the entity hosted by the tab provider.</span></span>     |
|  <span data-ttu-id="0aaa6-113">contentUrl</span><span class="sxs-lookup"><span data-stu-id="0aaa6-113">contentUrl</span></span> |   <span data-ttu-id="0aaa6-114">строка</span><span class="sxs-lookup"><span data-stu-id="0aaa6-114">string</span></span> |  <span data-ttu-id="0aaa6-115">URL-адрес, используемый для отображения содержимого вкладки в Teams.</span><span class="sxs-lookup"><span data-stu-id="0aaa6-115">Url used for rendering tab contents in Teams.</span></span> <span data-ttu-id="0aaa6-116">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="0aaa6-116">Required.</span></span>    |
|  <span data-ttu-id="0aaa6-117">removeUrl</span><span class="sxs-lookup"><span data-stu-id="0aaa6-117">removeUrl</span></span>  |   <span data-ttu-id="0aaa6-118">строка</span><span class="sxs-lookup"><span data-stu-id="0aaa6-118">string</span></span> |  <span data-ttu-id="0aaa6-119">URL-адрес, вызываемый клиентом Teams при удалении вкладки с помощью клиента Teams.</span><span class="sxs-lookup"><span data-stu-id="0aaa6-119">Url called by Teams client when a Tab is removed using the Teams Client.</span></span>     |
|  <span data-ttu-id="0aaa6-120">websiteUrl</span><span class="sxs-lookup"><span data-stu-id="0aaa6-120">websiteUrl</span></span> |   <span data-ttu-id="0aaa6-121">string</span><span class="sxs-lookup"><span data-stu-id="0aaa6-121">string</span></span> |  <span data-ttu-id="0aaa6-122">URL-адрес для отображения содержимого вкладки вне Teams.</span><span class="sxs-lookup"><span data-stu-id="0aaa6-122">Url for showing tab contents outside of Teams.</span></span>     |

## <a name="json-representation"></a><span data-ttu-id="0aaa6-123">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="0aaa6-123">JSON representation</span></span>

<span data-ttu-id="0aaa6-124">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="0aaa6-124">The following is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsTabConfiguration"
}-->

```json
{
   "entityId": "string",
   "contentUrl": "string (HTTPS Url)",
   "websiteUrl": "string (HTTPS Url)",
   "removeUrl": "string (HTTPS Url)"  
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "teamsTabConfiguration complex type (Open Type)",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/teamstabconfiguration.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
