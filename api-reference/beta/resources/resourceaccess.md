---
title: Тип ресурса Ресаурцеакцесс
description: Указывает область разрешений OAuth 2,0 или роль приложения, требуемую приложением.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: psignoret
ms.openlocfilehash: 6092a427a2882c4b6bdae07bb98f8bc8a81eecfb
ms.sourcegitcommit: 53a57f19a5b16029b540e61ddfba6c2b4e45cfc5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/06/2020
ms.locfileid: "44593634"
---
# <a name="resourceaccess-resource-type"></a><span data-ttu-id="c0e89-103">Тип ресурса Ресаурцеакцесс</span><span class="sxs-lookup"><span data-stu-id="c0e89-103">resourceAccess resource type</span></span>

<span data-ttu-id="c0e89-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="c0e89-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="c0e89-105">Указывает область разрешений OAuth 2,0 или роль приложения, требуемую приложением.</span><span class="sxs-lookup"><span data-stu-id="c0e89-105">Specifies an OAuth 2.0 permission scope or an app role that an application requires.</span></span> <span data-ttu-id="c0e89-106">Свойство **ресаурцеакцесс** типа [рекуиредресаурцеакцесс](requiredresourceaccess.md) является коллекцией **ресаурцеакцесс**.</span><span class="sxs-lookup"><span data-stu-id="c0e89-106">The **resourceAccess** property of the [requiredResourceAccess](requiredresourceaccess.md) type is a collection of **ResourceAccess**.</span></span>

## <a name="properties"></a><span data-ttu-id="c0e89-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0e89-107">Properties</span></span>
| <span data-ttu-id="c0e89-108">Свойство</span><span class="sxs-lookup"><span data-stu-id="c0e89-108">Property</span></span>     | <span data-ttu-id="c0e89-109">Тип</span><span class="sxs-lookup"><span data-stu-id="c0e89-109">Type</span></span>   |<span data-ttu-id="c0e89-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c0e89-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c0e89-111">id</span><span class="sxs-lookup"><span data-stu-id="c0e89-111">id</span></span>|<span data-ttu-id="c0e89-112">GUID</span><span class="sxs-lookup"><span data-stu-id="c0e89-112">Guid</span></span>|<span data-ttu-id="c0e89-113">Уникальный идентификатор для одного из экземпляров [oauth2PermissionScopes](permissionscope.md) или [аппроле](approle.md) , предоставляемых приложением ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0e89-113">The unique identifier for one of the [oauth2PermissionScopes](permissionscope.md) or [appRole](approle.md) instances that the resource application exposes.</span></span>|
|<span data-ttu-id="c0e89-114">type</span><span class="sxs-lookup"><span data-stu-id="c0e89-114">type</span></span>|<span data-ttu-id="c0e89-115">String</span><span class="sxs-lookup"><span data-stu-id="c0e89-115">String</span></span>|<span data-ttu-id="c0e89-116">Указывает, ссылается ли свойство **ID** на объект [oauth2PermissionScopes](permissionscope.md) или [аппроле](approle.md).</span><span class="sxs-lookup"><span data-stu-id="c0e89-116">Specifies whether the **id** property references an [oauth2PermissionScopes](permissionscope.md) or an [appRole](approle.md).</span></span> <span data-ttu-id="c0e89-117">Возможные значения: `Scope` или `Role` .</span><span class="sxs-lookup"><span data-stu-id="c0e89-117">Possible values are `Scope` or `Role`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c0e89-118">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="c0e89-118">JSON representation</span></span>

<span data-ttu-id="c0e89-119">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="c0e89-119">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.resourceAccess"
}-->

```json
{
  "id": "guid",
  "type": "string"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "resourceAccess resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
