---
title: Тип ресурса educationSubmissionIndividualRecipient
description: 'Подкласс educationSubmissionRecipient, которое указывает, что отправка назначен одному пользователю в классе.  '
ms.openlocfilehash: 4b74defc1a21427b6169e399262d827561178e5f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27075523"
---
# <a name="educationsubmissionindividualrecipient-resource-type"></a><span data-ttu-id="80e2a-103">Тип ресурса educationSubmissionIndividualRecipient</span><span class="sxs-lookup"><span data-stu-id="80e2a-103">educationSubmissionIndividualRecipient resource type</span></span>

> <span data-ttu-id="80e2a-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="80e2a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="80e2a-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="80e2a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="80e2a-106">Подкласс [educationSubmissionRecipient](educationsubmissionrecipient.md) , которое указывает, что отправка назначен одному пользователю в классе.</span><span class="sxs-lookup"><span data-stu-id="80e2a-106">A subclass of [educationSubmissionRecipient](educationsubmissionrecipient.md) that indicates that a submission is assigned to an individual in the class.</span></span>  


## <a name="properties"></a><span data-ttu-id="80e2a-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="80e2a-107">Properties</span></span>
| <span data-ttu-id="80e2a-108">Свойство</span><span class="sxs-lookup"><span data-stu-id="80e2a-108">Property</span></span>     | <span data-ttu-id="80e2a-109">Тип</span><span class="sxs-lookup"><span data-stu-id="80e2a-109">Type</span></span>   |<span data-ttu-id="80e2a-110">Description</span><span class="sxs-lookup"><span data-stu-id="80e2a-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="80e2a-111">userId</span><span class="sxs-lookup"><span data-stu-id="80e2a-111">userId</span></span>|<span data-ttu-id="80e2a-112">String</span><span class="sxs-lookup"><span data-stu-id="80e2a-112">String</span></span>|<span data-ttu-id="80e2a-113">Идентификатор пользователя, которому назначена подачи.</span><span class="sxs-lookup"><span data-stu-id="80e2a-113">User ID of the user to whom the submission is assigned.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="80e2a-114">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="80e2a-114">JSON representation</span></span>

<span data-ttu-id="80e2a-115">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="80e2a-115">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationSubmissionIndividualRecipient"
}-->

```json
{
  "userId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationSubmissionIndividualRecipient resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->