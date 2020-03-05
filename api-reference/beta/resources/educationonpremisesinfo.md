---
title: Тип ресурса Едукатиононпремисесинфо
description: Дополнительные сведения, используемые для сопоставления локальной учетной записи пользователя Active Directory с их объектом пользователя Azure AD.
author: mlafleur
localization_priority: Normal
ms.prod: education
doc_type: apiPageType
ms.openlocfilehash: 6695f1cd92ccde1fb26a581fce49c0c233deb141
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42501516"
---
# <a name="educationonpremisesinfo-resource-type"></a><span data-ttu-id="843b3-103">Тип ресурса Едукатиононпремисесинфо</span><span class="sxs-lookup"><span data-stu-id="843b3-103">educationOnPremisesInfo resource type</span></span>

<span data-ttu-id="843b3-104">Пространство имен: Microsoft. Graph</span><span class="sxs-lookup"><span data-stu-id="843b3-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="843b3-105">Дополнительные сведения, используемые для сопоставления локальной учетной записи пользователя Active Directory с их объектом пользователя Azure AD.</span><span class="sxs-lookup"><span data-stu-id="843b3-105">Additional information used to associate an on-premises Active Directory user account to their Azure AD user object.</span></span>

## <a name="properties"></a><span data-ttu-id="843b3-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="843b3-106">Properties</span></span>

| <span data-ttu-id="843b3-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="843b3-107">Property</span></span>    | <span data-ttu-id="843b3-108">Тип</span><span class="sxs-lookup"><span data-stu-id="843b3-108">Type</span></span>   | <span data-ttu-id="843b3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="843b3-109">Description</span></span>                                               |
| :---------- | :----- | :-------------------------------------------------------- |
| <span data-ttu-id="843b3-110">Значения свойств ImmutableId</span><span class="sxs-lookup"><span data-stu-id="843b3-110">immutableId</span></span> | <span data-ttu-id="843b3-111">String</span><span class="sxs-lookup"><span data-stu-id="843b3-111">String</span></span> | <span data-ttu-id="843b3-112">Уникальный идентификатор объекта пользователя в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="843b3-112">Unique identifier for the user object in Active Directory.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="843b3-113">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="843b3-113">JSON representation</span></span>

<span data-ttu-id="843b3-114">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="843b3-114">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationOnPremisesInfo"
}-->

```json
{
  "immutableId": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationOnPremisesInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
