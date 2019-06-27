---
title: Создание объекта appRoleAssignment
description: Используйте этот API для создания нового Аппролеассигнмент.
localization_priority: Normal
ms.openlocfilehash: 4c6090dc3b6efa4bf3929800d21c8bf67f17845d
ms.sourcegitcommit: 0e1101d499f35b08aa2309e273871438b1774979
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2019
ms.locfileid: "35269001"
---
# <a name="create-approleassignment"></a><span data-ttu-id="eaa77-103">Создание объекта appRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="eaa77-103">Create appRoleAssignment</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="eaa77-104">Используйте этот API для создания нового Аппролеассигнмент.</span><span class="sxs-lookup"><span data-stu-id="eaa77-104">Use this API to create a new appRoleAssignment.</span></span>

## <a name="permissions"></a><span data-ttu-id="eaa77-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="eaa77-105">Permissions</span></span>
<span data-ttu-id="eaa77-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eaa77-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eaa77-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="eaa77-108">Permission type</span></span>      | <span data-ttu-id="eaa77-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="eaa77-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eaa77-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="eaa77-110">Delegated (work or school account)</span></span> | <span data-ttu-id="eaa77-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="eaa77-111">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="eaa77-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="eaa77-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eaa77-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eaa77-113">Not supported.</span></span>    |
|<span data-ttu-id="eaa77-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="eaa77-114">Application</span></span> | <span data-ttu-id="eaa77-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eaa77-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="eaa77-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="eaa77-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/appRoleAssignments

```
## <a name="request-headers"></a><span data-ttu-id="eaa77-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="eaa77-117">Request headers</span></span>
| <span data-ttu-id="eaa77-118">Имя</span><span class="sxs-lookup"><span data-stu-id="eaa77-118">Name</span></span>       | <span data-ttu-id="eaa77-119">Тип</span><span class="sxs-lookup"><span data-stu-id="eaa77-119">Type</span></span> | <span data-ttu-id="eaa77-120">Описание</span><span class="sxs-lookup"><span data-stu-id="eaa77-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="eaa77-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="eaa77-121">Authorization</span></span>  | <span data-ttu-id="eaa77-122">string</span><span class="sxs-lookup"><span data-stu-id="eaa77-122">string</span></span>  | <span data-ttu-id="eaa77-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eaa77-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="eaa77-125">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="eaa77-125">Request body</span></span>
<span data-ttu-id="eaa77-126">В тексте запроса добавьте представление объекта [аппролеассигнмент](../resources/approleassignment.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="eaa77-126">In the request body, supply a JSON representation of [appRoleAssignment](../resources/approleassignment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="eaa77-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="eaa77-127">Response</span></span>

<span data-ttu-id="eaa77-128">В случае успешного выполнения этот метод `201 Created` возвращает код отклика и объект [аппролеассигнмент](../resources/approleassignment.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="eaa77-128">If successful, this method returns `201 Created` response code and [appRoleAssignment](../resources/approleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eaa77-129">Пример</span><span class="sxs-lookup"><span data-stu-id="eaa77-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eaa77-130">Запрос</span><span class="sxs-lookup"><span data-stu-id="eaa77-130">Request</span></span>
<span data-ttu-id="eaa77-131">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="eaa77-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_approleassignment_from_serviceprincipal"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/appRoleAssignments
Content-type: application/json
Content-length: 233

{
  "creationTimestamp": "2016-10-19T10:37:00Z",
  "principalDisplayName": "principalDisplayName-value",
  "principalId": "principalId-value",
  "principalType": "principalType-value",
  "resourceDisplayName": "resourceDisplayName-value"
}
```
<span data-ttu-id="eaa77-132">В тексте запроса добавьте представление объекта [аппролеассигнмент](../resources/approleassignment.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="eaa77-132">In the request body, supply a JSON representation of [appRoleAssignment](../resources/approleassignment.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="eaa77-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="eaa77-133">Response</span></span>
<span data-ttu-id="eaa77-p103">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="eaa77-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.appRoleAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 253

{
  "creationTimestamp": "2016-10-19T10:37:00Z",
  "id": "id-value",
  "principalDisplayName": "principalDisplayName-value",
  "principalId": "principalId-value",
  "principalType": "principalType-value",
  "resourceDisplayName": "resourceDisplayName-value"
}
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="eaa77-137">Пример кода SDK</span><span class="sxs-lookup"><span data-stu-id="eaa77-137">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="eaa77-138">C#</span><span class="sxs-lookup"><span data-stu-id="eaa77-138">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/create_approleassignment_from_serviceprincipal-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="eaa77-139">Javascript</span><span class="sxs-lookup"><span data-stu-id="eaa77-139">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/create_approleassignment_from_serviceprincipal-Javascript-snippets.md)]

# <a name="objective-ctabobjective-c"></a>[<span data-ttu-id="eaa77-140">Цель — C</span><span class="sxs-lookup"><span data-stu-id="eaa77-140">Objective-C</span></span>](#tab/objective-c)
[!INCLUDE [sample-code](../includes/create_approleassignment_from_serviceprincipal-Objective-C-snippets.md)]
---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create appRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/serviceprincipal-post-approleassignments.md:\r\n      BookmarkMissing: '[#tab/objective-c](Objective-C)'. Did you mean: #objective-c (score: 4)",
    "Error: /api-reference/beta/api/serviceprincipal-post-approleassignments.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/beta/api/serviceprincipal-post-approleassignments.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}
-->
