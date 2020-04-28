---
title: Тип ресурса Рекоммендлабелактион
description: Представляет метку, которая должна быть рекомендована пользователю для приложения в файл на основе типов конфиденциальной информации.
localization_priority: Normal
author: tommoser
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 2a4da2900ec12233e680238fb294c38a9e17ebbe
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42521238"
---
# <a name="recommendlabelaction-resource-type"></a><span data-ttu-id="0324d-103">Тип ресурса Рекоммендлабелактион</span><span class="sxs-lookup"><span data-stu-id="0324d-103">recommendLabelAction resource type</span></span>

<span data-ttu-id="0324d-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="0324d-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="0324d-105">Представляет метку, которая должна быть рекомендована пользователю для приложения в файл на основе обнаруженных типов конфиденциальной информации.</span><span class="sxs-lookup"><span data-stu-id="0324d-105">Represents a label that should be recommended to the user for application to the file based on discovered sensitive information types.</span></span> <span data-ttu-id="0324d-106">[Евалуатеклассификатионресултс](../api/informationprotectionlabel-evaluateClassificationResults.md) может возвращать **рекоммендлабелактион** , если для политики метки Microsoft Information Protection задано значение **рекомендовать** и подпись, а не задано применение метки.</span><span class="sxs-lookup"><span data-stu-id="0324d-106">The [evaluateClassificationResults](../api/informationprotectionlabel-evaluateClassificationResults.md) may return a **recommendLabelAction** if the Microsoft Information Protection labeling policy is set to **recommend** and label rather than enforce a label.</span></span> <span data-ttu-id="0324d-107">Пользователь или апплиатион может игнорировать или принять рекомендацию.</span><span class="sxs-lookup"><span data-stu-id="0324d-107">The user or appliation may choose to ignore or accept the recommendation.</span></span> 

## <a name="properties"></a><span data-ttu-id="0324d-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="0324d-108">Properties</span></span>

| <span data-ttu-id="0324d-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="0324d-109">Property</span></span>                    | <span data-ttu-id="0324d-110">Тип</span><span class="sxs-lookup"><span data-stu-id="0324d-110">Type</span></span>                                                                     | <span data-ttu-id="0324d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0324d-111">Description</span></span>                                                           |
| :-------------------------- | :----------------------------------------------------------------------- | :-------------------------------------------------------------------- |
| <span data-ttu-id="0324d-112">актионсаурце</span><span class="sxs-lookup"><span data-stu-id="0324d-112">actionSource</span></span>                | <span data-ttu-id="0324d-113">String</span><span class="sxs-lookup"><span data-stu-id="0324d-113">String</span></span>                                                                   | <span data-ttu-id="0324d-114">Возможные значения: `manual`, `automatic`, `recommended`, `default`.</span><span class="sxs-lookup"><span data-stu-id="0324d-114">Possible values are: `manual`, `automatic`, `recommended`, `default`.</span></span> |
| <span data-ttu-id="0324d-115">actions</span><span class="sxs-lookup"><span data-stu-id="0324d-115">actions</span></span>                     | <span data-ttu-id="0324d-116">Коллекция [информатионпротектионактион](informationprotectionaction.md)</span><span class="sxs-lookup"><span data-stu-id="0324d-116">[informationProtectionAction](informationprotectionaction.md) collection</span></span> | <span data-ttu-id="0324d-117">Действия, которые необходимо выполнить, если пользователь принимает метку.</span><span class="sxs-lookup"><span data-stu-id="0324d-117">Actions to take if the label is accepted by the user.</span></span>                                                                       |
| <span data-ttu-id="0324d-118">label</span><span class="sxs-lookup"><span data-stu-id="0324d-118">label</span></span>                       | [<span data-ttu-id="0324d-119">лабелдетаилс</span><span class="sxs-lookup"><span data-stu-id="0324d-119">labelDetails</span></span>](labeldetails.md)                                          | <span data-ttu-id="0324d-120">Рекомендуемая метка.</span><span class="sxs-lookup"><span data-stu-id="0324d-120">The label that is being recommended.</span></span>                                                                      |
| <span data-ttu-id="0324d-121">респонсиблесенситиветипеидс</span><span class="sxs-lookup"><span data-stu-id="0324d-121">responsibleSensitiveTypeIds</span></span> | <span data-ttu-id="0324d-122">Коллекция объектов Guid</span><span class="sxs-lookup"><span data-stu-id="0324d-122">Guid collection</span></span>                                                          | <span data-ttu-id="0324d-123">Идентификаторы GUID типа конфиденциальной информации, которые привели к выдано рекомендация.</span><span class="sxs-lookup"><span data-stu-id="0324d-123">The sensitive information type GUIDs that caused the recommendation to be given.</span></span>                                                                      |

## <a name="json-representation"></a><span data-ttu-id="0324d-124">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="0324d-124">JSON representation</span></span>

<span data-ttu-id="0324d-125">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="0324d-125">The following is a JSON representation of the resource.</span></span>

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
