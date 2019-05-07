---
title: 'message: replyAll'
description: Ответ всем получателям сообщения. Затем сообщение сохраняется в папке "Отправленные".
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 15a0587fc1749ecf168711f204f8a6397efe648d
ms.sourcegitcommit: b8d01acfc1cb7610a0e1f5c18065da415bae0777
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2019
ms.locfileid: "33612347"
---
# <a name="message-replyall"></a><span data-ttu-id="4c721-104">message: replyAll</span><span class="sxs-lookup"><span data-stu-id="4c721-104">message: replyAll</span></span>

<span data-ttu-id="4c721-p102">Ответ всем получателям сообщения. Затем сообщение сохраняется в папке "Отправленные".</span><span class="sxs-lookup"><span data-stu-id="4c721-p102">Reply to all recipients of a message. The message is then saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="4c721-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4c721-107">Permissions</span></span>
<span data-ttu-id="4c721-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4c721-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4c721-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="4c721-110">Permission type</span></span>      | <span data-ttu-id="4c721-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="4c721-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4c721-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="4c721-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4c721-113">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="4c721-113">Mail.Send</span></span>    |
|<span data-ttu-id="4c721-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="4c721-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4c721-115">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="4c721-115">Mail.Send</span></span>    |
|<span data-ttu-id="4c721-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="4c721-116">Application</span></span> | <span data-ttu-id="4c721-117">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="4c721-117">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="4c721-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="4c721-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/me/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/messages/{id}/replyAll
POST /me/mailFolders/{id}/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/replyAll
```
## <a name="request-headers"></a><span data-ttu-id="4c721-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="4c721-119">Request headers</span></span>
| <span data-ttu-id="4c721-120">Имя</span><span class="sxs-lookup"><span data-stu-id="4c721-120">Name</span></span>       | <span data-ttu-id="4c721-121">Тип</span><span class="sxs-lookup"><span data-stu-id="4c721-121">Type</span></span> | <span data-ttu-id="4c721-122">Описание</span><span class="sxs-lookup"><span data-stu-id="4c721-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4c721-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4c721-123">Authorization</span></span>  | <span data-ttu-id="4c721-124">string</span><span class="sxs-lookup"><span data-stu-id="4c721-124">string</span></span>  | <span data-ttu-id="4c721-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4c721-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4c721-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4c721-127">Content-Type</span></span> | <span data-ttu-id="4c721-128">string</span><span class="sxs-lookup"><span data-stu-id="4c721-128">string</span></span>  | <span data-ttu-id="4c721-p105">Характер данных в теле объекта. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4c721-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4c721-131">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="4c721-131">Request body</span></span>
<span data-ttu-id="4c721-132">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="4c721-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4c721-133">Параметр</span><span class="sxs-lookup"><span data-stu-id="4c721-133">Parameter</span></span>    | <span data-ttu-id="4c721-134">Тип</span><span class="sxs-lookup"><span data-stu-id="4c721-134">Type</span></span>   |<span data-ttu-id="4c721-135">Описание</span><span class="sxs-lookup"><span data-stu-id="4c721-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4c721-136">comment</span><span class="sxs-lookup"><span data-stu-id="4c721-136">comment</span></span>|<span data-ttu-id="4c721-137">String</span><span class="sxs-lookup"><span data-stu-id="4c721-137">String</span></span>|<span data-ttu-id="4c721-p106">Добавляемый комментарий. Может быть пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="4c721-p106">A comment to include. Can be an empty string.</span></span>|

## <a name="response"></a><span data-ttu-id="4c721-140">Отклик</span><span class="sxs-lookup"><span data-stu-id="4c721-140">Response</span></span>

<span data-ttu-id="4c721-p107">В случае успешного выполнения этот метод возвращает код отклика `202 Accepted`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="4c721-p107">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4c721-143">Пример</span><span class="sxs-lookup"><span data-stu-id="4c721-143">Example</span></span>
<span data-ttu-id="4c721-144">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="4c721-144">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="4c721-145">Запрос</span><span class="sxs-lookup"><span data-stu-id="4c721-145">Request</span></span>
<span data-ttu-id="4c721-146">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="4c721-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_replyall"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/replyAll
Content-type: application/json
Content-length: 32

{
  "comment": "comment-value"
}
```


##### <a name="response"></a><span data-ttu-id="4c721-147">Отклик</span><span class="sxs-lookup"><span data-stu-id="4c721-147">Response</span></span>
<span data-ttu-id="4c721-148">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="4c721-148">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="4c721-149">Пример кода для SDK</span><span class="sxs-lookup"><span data-stu-id="4c721-149">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="4c721-150">Языках</span><span class="sxs-lookup"><span data-stu-id="4c721-150">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/message_replyall-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="4c721-151">Язык</span><span class="sxs-lookup"><span data-stu-id="4c721-151">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/message_replyall-Javascript-snippets.md)]

---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: replyAll",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/v1.0/api/message-replyall.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/v1.0/api/message-replyall.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}-->
