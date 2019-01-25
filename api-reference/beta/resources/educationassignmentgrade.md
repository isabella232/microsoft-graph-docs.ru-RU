---
title: Тип ресурса educationAssignmentGrade
description: " Тем не менее являются подклассов это всех типов участников (точек, работоспособность и т.д.)"
localization_priority: Normal
author: dipakboyed
ms.prod: education
ms.openlocfilehash: 5ca13ba057ef000a468d910d49288d9ae8e0c962
ms.sourcegitcommit: 3d24047b3af46136734de2486b041e67a34f3d83
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "29527859"
---
# <a name="educationassignmentgrade-resource-type"></a><span data-ttu-id="943bb-103">Тип ресурса educationAssignmentGrade</span><span class="sxs-lookup"><span data-stu-id="943bb-103">educationAssignmentGrade resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="943bb-104">Представляет объект **марки** на отправку.</span><span class="sxs-lookup"><span data-stu-id="943bb-104">Represents the **Grade** object on a Submission.</span></span> <span data-ttu-id="943bb-105">Это абстрактный тип, никогда не будет создаваться; Тем не менее все типы участников (точек, работоспособность и т.д.), подклассов этого типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="943bb-105">This is an abstract type that will never be instantiated; however, all types of grading (points, pass/fail, and so on) are subclasses of this resource type.</span></span> <span data-ttu-id="943bb-106">Этот объект также отслеживает, который делает участников.</span><span class="sxs-lookup"><span data-stu-id="943bb-106">This object also tracks who is doing the grading.</span></span> <span data-ttu-id="943bb-107">Используется в свойстве **submission.grade** .</span><span class="sxs-lookup"><span data-stu-id="943bb-107">This is used in the **submission.grade** property.</span></span>


## <a name="properties"></a><span data-ttu-id="943bb-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="943bb-108">Properties</span></span>
| <span data-ttu-id="943bb-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="943bb-109">Property</span></span>     | <span data-ttu-id="943bb-110">Тип</span><span class="sxs-lookup"><span data-stu-id="943bb-110">Type</span></span>   |<span data-ttu-id="943bb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="943bb-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="943bb-112">gradedBy</span><span class="sxs-lookup"><span data-stu-id="943bb-112">gradedBy</span></span>|[<span data-ttu-id="943bb-113">identitySet</span><span class="sxs-lookup"><span data-stu-id="943bb-113">identitySet</span></span>](identityset.md)| <span data-ttu-id="943bb-114">Пользователь, который был участников.</span><span class="sxs-lookup"><span data-stu-id="943bb-114">User who did the grading.</span></span> |
|<span data-ttu-id="943bb-115">gradedDateTime</span><span class="sxs-lookup"><span data-stu-id="943bb-115">gradedDateTime</span></span>|<span data-ttu-id="943bb-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="943bb-116">DateTimeOffset</span></span>| <span data-ttu-id="943bb-117">Момент времени, когда марки была применена этот объект отправки.</span><span class="sxs-lookup"><span data-stu-id="943bb-117">Moment in time when the grade was applied to this submission object.</span></span> <span data-ttu-id="943bb-118">Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC).</span><span class="sxs-lookup"><span data-stu-id="943bb-118">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="943bb-119">Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="943bb-119">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|

## <a name="json-representation"></a><span data-ttu-id="943bb-120">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="943bb-120">JSON representation</span></span>

<span data-ttu-id="943bb-121">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="943bb-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationAssignmentGrade"
}-->

```json
{
  "gradedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "gradedDateTime": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "educationAssignmentGrade resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/educationassignmentgrade.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
