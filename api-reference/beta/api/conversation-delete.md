---
title: Удаление беседы
description: Удаление беседы.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
doc_type: apiPageType
ms.openlocfilehash: 7406bdc29d71903451d97fcaf4beee41994089ca
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48956898"
---
# <a name="delete-conversation"></a><span data-ttu-id="318ff-103">Удаление беседы</span><span class="sxs-lookup"><span data-stu-id="318ff-103">Delete conversation</span></span>

<span data-ttu-id="318ff-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="318ff-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="318ff-105">Удаление беседы.</span><span class="sxs-lookup"><span data-stu-id="318ff-105">Delete conversation.</span></span>
## <a name="permissions"></a><span data-ttu-id="318ff-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="318ff-106">Permissions</span></span>
<span data-ttu-id="318ff-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="318ff-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="318ff-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="318ff-109">Permission type</span></span>      | <span data-ttu-id="318ff-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="318ff-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="318ff-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="318ff-111">Delegated (work or school account)</span></span> | <span data-ttu-id="318ff-112">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="318ff-112">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="318ff-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="318ff-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="318ff-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="318ff-114">Not supported.</span></span>    |
|<span data-ttu-id="318ff-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="318ff-115">Application</span></span> | <span data-ttu-id="318ff-116">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="318ff-116">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="318ff-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="318ff-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/conversations/{id}
```
## <a name="request-headers"></a><span data-ttu-id="318ff-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="318ff-118">Request headers</span></span>
| <span data-ttu-id="318ff-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="318ff-119">Header</span></span>       | <span data-ttu-id="318ff-120">Значение</span><span class="sxs-lookup"><span data-stu-id="318ff-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="318ff-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="318ff-121">Authorization</span></span>  | <span data-ttu-id="318ff-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="318ff-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="318ff-124">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="318ff-124">Request body</span></span>
<span data-ttu-id="318ff-125">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="318ff-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="318ff-126">Отклик</span><span class="sxs-lookup"><span data-stu-id="318ff-126">Response</span></span>

<span data-ttu-id="318ff-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="318ff-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="318ff-129">Пример</span><span class="sxs-lookup"><span data-stu-id="318ff-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="318ff-130">Запрос</span><span class="sxs-lookup"><span data-stu-id="318ff-130">Request</span></span>
<span data-ttu-id="318ff-131">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="318ff-131">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="318ff-132">HTTP</span><span class="sxs-lookup"><span data-stu-id="318ff-132">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_conversation"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/{id}/conversations/{id}
```
# <a name="c"></a>[<span data-ttu-id="318ff-133">C#</span><span class="sxs-lookup"><span data-stu-id="318ff-133">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-conversation-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="318ff-134">JavaScript</span><span class="sxs-lookup"><span data-stu-id="318ff-134">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-conversation-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="318ff-135">Objective-C</span><span class="sxs-lookup"><span data-stu-id="318ff-135">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-conversation-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="318ff-136">Java</span><span class="sxs-lookup"><span data-stu-id="318ff-136">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-conversation-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="318ff-137">Отклик</span><span class="sxs-lookup"><span data-stu-id="318ff-137">Response</span></span>
<span data-ttu-id="318ff-138">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="318ff-138">Here is an example of the response.</span></span> 
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
  "description": "Delete conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


