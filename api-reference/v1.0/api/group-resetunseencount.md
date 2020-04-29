---
title: 'group: resetUnseenCount'
description: Сброс unseenCount всех записей, которые текущий пользователь не просматривал со времени своего предыдущего посещения. Поддерживается только для групп Office 365.
author: yyuank
localization_priority: Normal
ms.prod: groups
doc_type: apiPageType
ms.openlocfilehash: d0b6207eaa0329a1f664298955a57f2d6fbb1e9a
ms.sourcegitcommit: 1bc5a0c179dce57e90349610566fb86e1b5fbf95
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/04/2020
ms.locfileid: "43144256"
---
# <a name="group-resetunseencount"></a><span data-ttu-id="603ad-104">group: resetUnseenCount</span><span class="sxs-lookup"><span data-stu-id="603ad-104">group: resetUnseenCount</span></span>

<span data-ttu-id="603ad-105">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="603ad-105">Namespace: microsoft.graph</span></span>

<span data-ttu-id="603ad-p102">Сброс unseenCount всех записей, которые текущий пользователь не просматривал со времени своего предыдущего посещения. Поддерживается только для групп Office 365.</span><span class="sxs-lookup"><span data-stu-id="603ad-p102">Reset the unseenCount of all the posts that the current user has not seen since their last visit. Supported for Office 365 groups only.</span></span>

## <a name="permissions"></a><span data-ttu-id="603ad-108">Разрешения</span><span class="sxs-lookup"><span data-stu-id="603ad-108">Permissions</span></span>
<span data-ttu-id="603ad-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="603ad-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="603ad-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="603ad-111">Permission type</span></span>      | <span data-ttu-id="603ad-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="603ad-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="603ad-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="603ad-113">Delegated (work or school account)</span></span> | <span data-ttu-id="603ad-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="603ad-114">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="603ad-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="603ad-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="603ad-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="603ad-116">Not supported.</span></span>    |
|<span data-ttu-id="603ad-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="603ad-117">Application</span></span> | <span data-ttu-id="603ad-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="603ad-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="603ad-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="603ad-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/resetUnseenCount
```
## <a name="request-headers"></a><span data-ttu-id="603ad-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="603ad-120">Request headers</span></span>
| <span data-ttu-id="603ad-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="603ad-121">Header</span></span>       | <span data-ttu-id="603ad-122">Значение</span><span class="sxs-lookup"><span data-stu-id="603ad-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="603ad-123">Авторизация</span><span class="sxs-lookup"><span data-stu-id="603ad-123">Authorization</span></span>  | <span data-ttu-id="603ad-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="603ad-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="603ad-126">Prefer</span><span class="sxs-lookup"><span data-stu-id="603ad-126">Prefer</span></span> | <span data-ttu-id="603ad-127">return=minimal.</span><span class="sxs-lookup"><span data-stu-id="603ad-127">return=minimal.</span></span> <span data-ttu-id="603ad-128">Если заголовок минимального отклика включен в заголовок запроса, то в отклике об успешном выполнении возвращается код `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="603ad-128">If minimal response header is included in the request header, then a successful response returns `204 No Content` code.</span></span> <span data-ttu-id="603ad-129">Необязательное свойство.</span><span class="sxs-lookup"><span data-stu-id="603ad-129">Optional.</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="603ad-130">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="603ad-130">Request body</span></span>
<span data-ttu-id="603ad-131">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="603ad-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="603ad-132">Ответ</span><span class="sxs-lookup"><span data-stu-id="603ad-132">Response</span></span>
<span data-ttu-id="603ad-p106">В случае успешного выполнения этот метод возвращает код отклика `200 OK`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="603ad-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="603ad-135">Пример</span><span class="sxs-lookup"><span data-stu-id="603ad-135">Example</span></span>
#### <a name="request"></a><span data-ttu-id="603ad-136">Запрос</span><span class="sxs-lookup"><span data-stu-id="603ad-136">Request</span></span>
<span data-ttu-id="603ad-137">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="603ad-137">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="603ad-138">HTTP</span><span class="sxs-lookup"><span data-stu-id="603ad-138">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "group_resetunseencount"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/resetUnseenCount
```
# <a name="c"></a>[<span data-ttu-id="603ad-139">C#</span><span class="sxs-lookup"><span data-stu-id="603ad-139">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/group-resetunseencount-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="603ad-140">JavaScript</span><span class="sxs-lookup"><span data-stu-id="603ad-140">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/group-resetunseencount-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="603ad-141">Objective-C</span><span class="sxs-lookup"><span data-stu-id="603ad-141">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/group-resetunseencount-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="603ad-142">Java</span><span class="sxs-lookup"><span data-stu-id="603ad-142">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/group-resetunseencount-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a><span data-ttu-id="603ad-143">Отклик</span><span class="sxs-lookup"><span data-stu-id="603ad-143">Response</span></span>
<span data-ttu-id="603ad-144">Ниже приведен пример ответа.</span><span class="sxs-lookup"><span data-stu-id="603ad-144">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: resetUnseenCount",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
