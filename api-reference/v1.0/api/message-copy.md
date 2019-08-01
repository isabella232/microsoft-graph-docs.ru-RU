---
title: 'message: copy'
description: Копирование сообщения в папку.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: 37c5571b337a4501ca25c8b04fde8d2a0f7ba4cb
ms.sourcegitcommit: 2c62457e57467b8d50f21b255b553106a9a5d8d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2019
ms.locfileid: "36022945"
---
# <a name="message-copy"></a><span data-ttu-id="c5c9c-103">message: copy</span><span class="sxs-lookup"><span data-stu-id="c5c9c-103">message: copy</span></span>

<span data-ttu-id="c5c9c-104">Копирование сообщения в папку.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-104">Copy a message to a folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="c5c9c-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="c5c9c-105">Permissions</span></span>

<span data-ttu-id="c5c9c-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c5c9c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="c5c9c-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="c5c9c-108">Permission type</span></span> | <span data-ttu-id="c5c9c-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="c5c9c-109">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="c5c9c-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c5c9c-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c5c9c-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c5c9c-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c5c9c-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="c5c9c-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c5c9c-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c5c9c-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c5c9c-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="c5c9c-114">Application</span></span> | <span data-ttu-id="c5c9c-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c5c9c-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c5c9c-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="c5c9c-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/copy
POST /users/{id | userPrincipalName}/messages/{id}/copy
POST /me/mailFolders/{id}/messages/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/copy
```

## <a name="request-headers"></a><span data-ttu-id="c5c9c-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="c5c9c-117">Request headers</span></span>

| <span data-ttu-id="c5c9c-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c5c9c-118">Header</span></span> | <span data-ttu-id="c5c9c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c5c9c-119">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="c5c9c-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="c5c9c-120">Authorization</span></span> | <span data-ttu-id="c5c9c-121">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-121"></span></span> <span data-ttu-id="c5c9c-122">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-122">Required.</span></span> |
| <span data-ttu-id="c5c9c-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c5c9c-123">Content-Type</span></span> | <span data-ttu-id="c5c9c-124">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-124"></span></span> <span data-ttu-id="c5c9c-125">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-125">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c5c9c-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="c5c9c-126">Request body</span></span>

<span data-ttu-id="c5c9c-127">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c5c9c-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="c5c9c-128">Parameter</span></span> | <span data-ttu-id="c5c9c-129">Тип</span><span class="sxs-lookup"><span data-stu-id="c5c9c-129">Type</span></span> | <span data-ttu-id="c5c9c-130">Описание</span><span class="sxs-lookup"><span data-stu-id="c5c9c-130">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="c5c9c-131">destinationId</span><span class="sxs-lookup"><span data-stu-id="c5c9c-131">destinationId</span></span>|<span data-ttu-id="c5c9c-132">String</span><span class="sxs-lookup"><span data-stu-id="c5c9c-132">String</span></span>|<span data-ttu-id="c5c9c-133">Идентификатор целевой папки либо имя известной папки.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-133">The destination folder ID, or a well-known folder name.</span></span> <span data-ttu-id="c5c9c-134">Список поддерживаемых известных имен см. в статье [Тип ресурса mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="c5c9c-134">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="c5c9c-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="c5c9c-135">Response</span></span>

<span data-ttu-id="c5c9c-136">В случае успеха этот метод возвращает код отклика `201 Created` и ресурс [message](../resources/message.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-136">If successful, this method returns `201 Created` response code and a [message](../resources/message.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c5c9c-137">Пример</span><span class="sxs-lookup"><span data-stu-id="c5c9c-137">Example</span></span>

<span data-ttu-id="c5c9c-138">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-138">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="c5c9c-139">Запрос</span><span class="sxs-lookup"><span data-stu-id="c5c9c-139">Request</span></span>
<span data-ttu-id="c5c9c-140">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-140">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="c5c9c-141">HTTP</span><span class="sxs-lookup"><span data-stu-id="c5c9c-141">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "message_copy"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/copy
Content-type: application/json
Content-length: 44

{
  "destinationId": "destinationId-value"
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="c5c9c-142">C#</span><span class="sxs-lookup"><span data-stu-id="c5c9c-142">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/message-copy-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="c5c9c-143">Javascript</span><span class="sxs-lookup"><span data-stu-id="c5c9c-143">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/message-copy-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="c5c9c-144">Цель — C</span><span class="sxs-lookup"><span data-stu-id="c5c9c-144">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/message-copy-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="c5c9c-145">Java</span><span class="sxs-lookup"><span data-stu-id="c5c9c-145">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/message-copy-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="c5c9c-146">Ответ</span><span class="sxs-lookup"><span data-stu-id="c5c9c-146">Response</span></span>

<span data-ttu-id="c5c9c-147">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-147">Here is an example of the response.</span></span>

> <span data-ttu-id="c5c9c-148">**Примечание.**  Представленный здесь объект ответа может быть сокращен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-148">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="c5c9c-149">При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="c5c9c-149">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: copy",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
