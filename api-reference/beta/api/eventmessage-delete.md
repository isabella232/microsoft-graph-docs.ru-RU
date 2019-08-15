---
title: Удаление объекта eventMessage
description: Удаление объекта eventMessage.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: f9a5a55f56e2e4cab47efb95fe33cae07d6b6938
ms.sourcegitcommit: 1066aa4045d48f9c9b764d3b2891cf4f806d17d5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2019
ms.locfileid: "36419848"
---
# <a name="delete-eventmessage"></a><span data-ttu-id="bbed6-103">Удаление объекта eventMessage</span><span class="sxs-lookup"><span data-stu-id="bbed6-103">Delete eventMessage</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="bbed6-104">Удаление объекта eventMessage.</span><span class="sxs-lookup"><span data-stu-id="bbed6-104">Delete eventMessage.</span></span>
## <a name="permissions"></a><span data-ttu-id="bbed6-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="bbed6-105">Permissions</span></span>
<span data-ttu-id="bbed6-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bbed6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bbed6-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="bbed6-108">Permission type</span></span>      | <span data-ttu-id="bbed6-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="bbed6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bbed6-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="bbed6-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bbed6-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bbed6-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="bbed6-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="bbed6-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bbed6-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bbed6-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="bbed6-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="bbed6-114">Application</span></span> | <span data-ttu-id="bbed6-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bbed6-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="bbed6-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="bbed6-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}

DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="bbed6-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="bbed6-117">Request headers</span></span>
| <span data-ttu-id="bbed6-118">Имя</span><span class="sxs-lookup"><span data-stu-id="bbed6-118">Name</span></span>       | <span data-ttu-id="bbed6-119">Тип</span><span class="sxs-lookup"><span data-stu-id="bbed6-119">Type</span></span> | <span data-ttu-id="bbed6-120">Описание</span><span class="sxs-lookup"><span data-stu-id="bbed6-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="bbed6-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="bbed6-121">Authorization</span></span>  | <span data-ttu-id="bbed6-122">string</span><span class="sxs-lookup"><span data-stu-id="bbed6-122">string</span></span>  | <span data-ttu-id="bbed6-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="bbed6-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bbed6-125">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="bbed6-125">Request body</span></span>
<span data-ttu-id="bbed6-126">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="bbed6-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bbed6-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="bbed6-127">Response</span></span>

<span data-ttu-id="bbed6-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="bbed6-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bbed6-130">Пример</span><span class="sxs-lookup"><span data-stu-id="bbed6-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bbed6-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="bbed6-131">Request</span></span>
<span data-ttu-id="bbed6-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="bbed6-132">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="bbed6-133">HTTP</span><span class="sxs-lookup"><span data-stu-id="bbed6-133">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_eventmessage"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/messages/{id}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="bbed6-134">C#</span><span class="sxs-lookup"><span data-stu-id="bbed6-134">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-eventmessage-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="bbed6-135">JavaScript</span><span class="sxs-lookup"><span data-stu-id="bbed6-135">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-eventmessage-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="bbed6-136">Цель — C</span><span class="sxs-lookup"><span data-stu-id="bbed6-136">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-eventmessage-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="bbed6-137">Отклик</span><span class="sxs-lookup"><span data-stu-id="bbed6-137">Response</span></span>
<span data-ttu-id="bbed6-138">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="bbed6-138">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Delete eventMessage",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
