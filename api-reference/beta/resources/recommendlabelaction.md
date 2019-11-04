---
title: Тип ресурса Рекоммендлабелактион
description: Представляет метку, которая должна быть рекомендована пользователю для приложения в файл на основе типов конфиденциальной информации.
localization_priority: Normal
author: tommoser
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 54f2a872c0aa64eb79e0b8755ddc6b3788f14055
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "37939378"
---
# <a name="recommendlabelaction-resource-type"></a><span data-ttu-id="b7f78-103">Тип ресурса Рекоммендлабелактион</span><span class="sxs-lookup"><span data-stu-id="b7f78-103">recommendLabelAction resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="b7f78-104">Представляет метку, которая должна быть рекомендована пользователю для приложения в файл на основе обнаруженных типов конфиденциальной информации.</span><span class="sxs-lookup"><span data-stu-id="b7f78-104">Represents a label that should be recommended to the user for application to the file based on discovered sensitive information types.</span></span> <span data-ttu-id="b7f78-105">[Евалуатеклассификатионресултс](../api/informationprotectionlabel-evaluateClassificationResults.md) может возвращать **рекоммендлабелактион** , если для политики метки Microsoft Information Protection задано значение **рекомендовать** и подпись, а не задано применение метки.</span><span class="sxs-lookup"><span data-stu-id="b7f78-105">The [evaluateClassificationResults](../api/informationprotectionlabel-evaluateClassificationResults.md) may return a **recommendLabelAction** if the Microsoft Information Protection labeling policy is set to **recommend** and label rather than enforce a label.</span></span> <span data-ttu-id="b7f78-106">Пользователь или апплиатион может игнорировать или принять рекомендацию.</span><span class="sxs-lookup"><span data-stu-id="b7f78-106">The user or appliation may choose to ignore or accept the recommendation.</span></span> 

## <a name="properties"></a><span data-ttu-id="b7f78-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7f78-107">Properties</span></span>

| <span data-ttu-id="b7f78-108">Свойство</span><span class="sxs-lookup"><span data-stu-id="b7f78-108">Property</span></span>                    | <span data-ttu-id="b7f78-109">Тип</span><span class="sxs-lookup"><span data-stu-id="b7f78-109">Type</span></span>                                                                     | <span data-ttu-id="b7f78-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b7f78-110">Description</span></span>                                                           |
| :-------------------------- | :----------------------------------------------------------------------- | :-------------------------------------------------------------------- |
| <span data-ttu-id="b7f78-111">актионсаурце</span><span class="sxs-lookup"><span data-stu-id="b7f78-111">actionSource</span></span>                | <span data-ttu-id="b7f78-112">String</span><span class="sxs-lookup"><span data-stu-id="b7f78-112">String</span></span>                                                                   | <span data-ttu-id="b7f78-113">Возможные значения: `manual`, `automatic`, `recommended`, `default`.</span><span class="sxs-lookup"><span data-stu-id="b7f78-113">Possible values are: `manual`, `automatic`, `recommended`, `default`.</span></span> |
| <span data-ttu-id="b7f78-114">actions</span><span class="sxs-lookup"><span data-stu-id="b7f78-114">actions</span></span>                     | <span data-ttu-id="b7f78-115">Коллекция [информатионпротектионактион](informationprotectionaction.md)</span><span class="sxs-lookup"><span data-stu-id="b7f78-115">[informationProtectionAction](informationprotectionaction.md) collection</span></span> | <span data-ttu-id="b7f78-116">Действия, которые необходимо выполнить, если пользователь принимает метку.</span><span class="sxs-lookup"><span data-stu-id="b7f78-116">Actions to take if the label is accepted by the user.</span></span>                                                                       |
| <span data-ttu-id="b7f78-117">label</span><span class="sxs-lookup"><span data-stu-id="b7f78-117">label</span></span>                       | [<span data-ttu-id="b7f78-118">лабелдетаилс</span><span class="sxs-lookup"><span data-stu-id="b7f78-118">labelDetails</span></span>](labeldetails.md)                                          | <span data-ttu-id="b7f78-119">Рекомендуемая метка.</span><span class="sxs-lookup"><span data-stu-id="b7f78-119">The label that is being recommended.</span></span>                                                                      |
| <span data-ttu-id="b7f78-120">респонсиблесенситиветипеидс</span><span class="sxs-lookup"><span data-stu-id="b7f78-120">responsibleSensitiveTypeIds</span></span> | <span data-ttu-id="b7f78-121">Коллекция объектов Guid</span><span class="sxs-lookup"><span data-stu-id="b7f78-121">Guid collection</span></span>                                                          | <span data-ttu-id="b7f78-122">Идентификаторы GUID типа конфиденциальной информации, которые привели к выдано рекомендация.</span><span class="sxs-lookup"><span data-stu-id="b7f78-122">The sensitive information type GUIDs that caused the recommendation to be given.</span></span>                                                                      |

## <a name="json-representation"></a><span data-ttu-id="b7f78-123">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="b7f78-123">JSON representation</span></span>

<span data-ttu-id="b7f78-124">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="b7f78-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recommendLabelAction",
  "baseType": "microsoft.graph.informationProtectionAction"
}-->

```json
{
  "actionSource": "String",
  "actions": [{"@odata.type": "microsoft.graph.informationProtectionAction"}],
  "label": {"@odata.type": "microsoft.graph.labelDetails"},
  "responsibleSensitiveTypeIds": ["Guid"]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recommendLabelAction resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
