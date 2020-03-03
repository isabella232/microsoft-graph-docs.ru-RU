---
title: Тип ресурса ПровисионингсервицепринЦипал
description: Представляет участника службы, используемого для подготовки.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 59dd514ff818ee37b462d8f21f3dce02d213eb20
ms.sourcegitcommit: d3b6e4d11012e6b4c775afcec4fe5444e3a99bd3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2020
ms.locfileid: "42394782"
---
# <a name="provisioningserviceprincipal-resource-type"></a><span data-ttu-id="d4a82-103">Тип ресурса ПровисионингсервицепринЦипал</span><span class="sxs-lookup"><span data-stu-id="d4a82-103">provisioningServicePrincipal resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="d4a82-104">Представляет участника службы, используемого для подготовки.</span><span class="sxs-lookup"><span data-stu-id="d4a82-104">Represents the service principal used for provisioning.</span></span> 

## <a name="properties"></a><span data-ttu-id="d4a82-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="d4a82-105">Properties</span></span>

| <span data-ttu-id="d4a82-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="d4a82-106">Property</span></span>     | <span data-ttu-id="d4a82-107">Тип</span><span class="sxs-lookup"><span data-stu-id="d4a82-107">Type</span></span>        | <span data-ttu-id="d4a82-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d4a82-108">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="d4a82-109">id</span><span class="sxs-lookup"><span data-stu-id="d4a82-109">id</span></span>|<span data-ttu-id="d4a82-110">Строка</span><span class="sxs-lookup"><span data-stu-id="d4a82-110">String</span></span>|<span data-ttu-id="d4a82-111">Уникально идентифицирует **servicePrincipal** , используемый для подготовки.</span><span class="sxs-lookup"><span data-stu-id="d4a82-111">Uniquely identifies the **servicePrincipal** used for provisioning.</span></span>|
|<span data-ttu-id="d4a82-112">name</span><span class="sxs-lookup"><span data-stu-id="d4a82-112">name</span></span>|<span data-ttu-id="d4a82-113">String</span><span class="sxs-lookup"><span data-stu-id="d4a82-113">String</span></span>| <span data-ttu-id="d4a82-114">Определяемое пользователем имя для **servicePrincipal**.</span><span class="sxs-lookup"><span data-stu-id="d4a82-114">Customer-defined name for the **servicePrincipal**.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d4a82-115">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="d4a82-115">JSON representation</span></span>

<span data-ttu-id="d4a82-116">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="d4a82-116">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.provisioningServicePrincipal",
  "baseType": null
}-->

```json
{
  "id": "String",
  "name": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "provisioningServicePrincipal resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
