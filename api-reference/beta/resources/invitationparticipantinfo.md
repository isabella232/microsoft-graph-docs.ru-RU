---
title: Тип ресурса ИнвитатионпартиЦипантинфо
description: Представляет объект, приглашенный на вызов группы.
author: VinodRavichandran
localization_priority: Normal
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: bddce0358bfa0ec46d8231958817002cb4ca8c20
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40870224"
---
# <a name="invitationparticipantinfo-resource-type"></a><span data-ttu-id="ba7df-103">Тип ресурса ИнвитатионпартиЦипантинфо</span><span class="sxs-lookup"><span data-stu-id="ba7df-103">invitationParticipantInfo resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="ba7df-104">Представляет объект, приглашенный на вызов группы.</span><span class="sxs-lookup"><span data-stu-id="ba7df-104">Represents an entity that is being invited to a group call.</span></span> 

## <a name="properties"></a><span data-ttu-id="ba7df-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba7df-105">Properties</span></span>

| <span data-ttu-id="ba7df-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="ba7df-106">Property</span></span>                           | <span data-ttu-id="ba7df-107">Тип</span><span class="sxs-lookup"><span data-stu-id="ba7df-107">Type</span></span>                          | <span data-ttu-id="ba7df-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ba7df-108">Description</span></span>                                                                          |
| :--------------------------------- | :---------------------------- | :----------------------------------------------------------------------------------- |
| <span data-ttu-id="ba7df-109">ендпоинттипе</span><span class="sxs-lookup"><span data-stu-id="ba7df-109">endpointType</span></span>                       | <span data-ttu-id="ba7df-110">String</span><span class="sxs-lookup"><span data-stu-id="ba7df-110">String</span></span>                        | <span data-ttu-id="ba7df-111">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ba7df-111">The type of endpoint.</span></span> <span data-ttu-id="ba7df-112">Возможные значения: `default`, `voicemail`.</span><span class="sxs-lookup"><span data-stu-id="ba7df-112">Possible values are: `default`, `voicemail`.</span></span> |
| <span data-ttu-id="ba7df-113">хищения</span><span class="sxs-lookup"><span data-stu-id="ba7df-113">identity</span></span>                           | [<span data-ttu-id="ba7df-114">identitySet</span><span class="sxs-lookup"><span data-stu-id="ba7df-114">identitySet</span></span>](identityset.md) | <span data-ttu-id="ba7df-115">[Удостоверение](identityset.md) , связанное с этим приглашением.</span><span class="sxs-lookup"><span data-stu-id="ba7df-115">The [identitySet](identityset.md) associated with this invitation.</span></span>                   |
| <span data-ttu-id="ba7df-116">реплацескаллид</span><span class="sxs-lookup"><span data-stu-id="ba7df-116">replacesCallId</span></span>                     | <span data-ttu-id="ba7df-117">String</span><span class="sxs-lookup"><span data-stu-id="ba7df-117">String</span></span>                        | <span data-ttu-id="ba7df-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="ba7df-118">Optional.</span></span> <span data-ttu-id="ba7df-119">Вызов, частью которого в данный момент является целевой иденити.</span><span class="sxs-lookup"><span data-stu-id="ba7df-119">The call which the target idenity is currently a part of.</span></span> <span data-ttu-id="ba7df-120">Этот вызов будет сброшен после добавления участника.</span><span class="sxs-lookup"><span data-stu-id="ba7df-120">This call will be dropped once the participant is added.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ba7df-121">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="ba7df-121">JSON representation</span></span>

<span data-ttu-id="ba7df-122">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="ba7df-122">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "endpointType",
    "replacesCallId"
  ],
  "@odata.type": "microsoft.graph.invitationParticipantInfo"
}-->
```json
{
  "endpointType": "default | voicemail",
  "identity": {"@odata.type": "#microsoft.graph.identitySet"},
  "replacesCallId": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "invitationParticipantInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
