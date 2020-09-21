---
title: 'conversationThread: reply'
description: 'Ответ на цепочку в беседе группы и добавление в нее новой записи. Вы можете указать родительскую беседу. '
author: dkershaw10
localization_priority: Normal
ms.prod: groups
doc_type: apiPageType
ms.openlocfilehash: 20dbb5c9734777ba127419c4fbcb1602131467ff
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48009984"
---
# <a name="conversationthread-reply"></a><span data-ttu-id="44734-104">conversationThread: reply</span><span class="sxs-lookup"><span data-stu-id="44734-104">conversationThread: reply</span></span>

<span data-ttu-id="44734-105">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="44734-105">Namespace: microsoft.graph</span></span>

<span data-ttu-id="44734-p102">Ответ на цепочку в беседе группы и добавление в нее новой записи. Вы можете указать в запросе всю родительскую беседу или только цепочку.</span><span class="sxs-lookup"><span data-stu-id="44734-p102">Reply to a thread in a group conversation and add a new post to it. You can specify the parent conversation in the request, or, you can specify just the thread without the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="44734-108">Разрешения</span><span class="sxs-lookup"><span data-stu-id="44734-108">Permissions</span></span>
<span data-ttu-id="44734-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="44734-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="44734-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="44734-111">Permission type</span></span>      | <span data-ttu-id="44734-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="44734-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="44734-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="44734-113">Delegated (work or school account)</span></span> | <span data-ttu-id="44734-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="44734-114">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="44734-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="44734-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="44734-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="44734-116">Not supported.</span></span>    |
|<span data-ttu-id="44734-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="44734-117">Application</span></span> | <span data-ttu-id="44734-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="44734-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="44734-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="44734-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/reply
```
## <a name="request-headers"></a><span data-ttu-id="44734-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="44734-120">Request headers</span></span>
| <span data-ttu-id="44734-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="44734-121">Header</span></span>       | <span data-ttu-id="44734-122">Значение</span><span class="sxs-lookup"><span data-stu-id="44734-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="44734-123">Авторизация</span><span class="sxs-lookup"><span data-stu-id="44734-123">Authorization</span></span>  | <span data-ttu-id="44734-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="44734-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="44734-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="44734-126">Content-Type</span></span>  | <span data-ttu-id="44734-p105">application/json. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="44734-p105">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="44734-129">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="44734-129">Request body</span></span>
<span data-ttu-id="44734-130">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="44734-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="44734-131">Параметр</span><span class="sxs-lookup"><span data-stu-id="44734-131">Parameter</span></span>    | <span data-ttu-id="44734-132">Тип</span><span class="sxs-lookup"><span data-stu-id="44734-132">Type</span></span>   |<span data-ttu-id="44734-133">Описание</span><span class="sxs-lookup"><span data-stu-id="44734-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="44734-134">post</span><span class="sxs-lookup"><span data-stu-id="44734-134">post</span></span>|[<span data-ttu-id="44734-135">post</span><span class="sxs-lookup"><span data-stu-id="44734-135">post</span></span>](../resources/post.md)|<span data-ttu-id="44734-136">Новая запись для ответа.</span><span class="sxs-lookup"><span data-stu-id="44734-136">The new post that is being replied with.</span></span>|

## <a name="response"></a><span data-ttu-id="44734-137">Отклик</span><span class="sxs-lookup"><span data-stu-id="44734-137">Response</span></span>

<span data-ttu-id="44734-p106">В случае успешного выполнения этот метод возвращает код отклика `202 Accepted`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="44734-p106">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="44734-140">Пример</span><span class="sxs-lookup"><span data-stu-id="44734-140">Example</span></span>
<span data-ttu-id="44734-141">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="44734-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="44734-142">Запрос</span><span class="sxs-lookup"><span data-stu-id="44734-142">Request</span></span>
<span data-ttu-id="44734-143">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="44734-143">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="44734-144">HTTP</span><span class="sxs-lookup"><span data-stu-id="44734-144">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "conversationthread_reply"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/reply
Content-type: application/json
Content-length: 1131

{
  "post": {
    "body": {
      "contentType": "",
      "content": "content-value"
    }
  }
}
```
# <a name="c"></a>[<span data-ttu-id="44734-145">C#</span><span class="sxs-lookup"><span data-stu-id="44734-145">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/conversationthread-reply-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="44734-146">JavaScript</span><span class="sxs-lookup"><span data-stu-id="44734-146">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/conversationthread-reply-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="44734-147">Java</span><span class="sxs-lookup"><span data-stu-id="44734-147">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/conversationthread-reply-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="44734-148">Отклик</span><span class="sxs-lookup"><span data-stu-id="44734-148">Response</span></span>
<span data-ttu-id="44734-149">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="44734-149">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conversationThread: reply",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->

