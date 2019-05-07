---
title: Удаление сообщения
description: Удаление сообщения из почтового ящика указанного пользователя или удаление связи сообщения.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 2fd5621901c8455bfa478c2fb5849b0b781470bc
ms.sourcegitcommit: b8d01acfc1cb7610a0e1f5c18065da415bae0777
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2019
ms.locfileid: "33612858"
---
# <a name="delete-message"></a><span data-ttu-id="e6eee-103">Удаление сообщения</span><span class="sxs-lookup"><span data-stu-id="e6eee-103">Delete message</span></span>

<span data-ttu-id="e6eee-104">Удаление сообщения из почтового ящика указанного пользователя или удаление связи сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6eee-104">Delete a message in the specified user's mailbox, or delete a relationship of the message.</span></span>

><span data-ttu-id="e6eee-105">**Note (Примечание** ) Удаление элементов из папки "удаления элементов с возможностью восстановления" может быть недоступно (представлено известным [именем](../resources/mailfolder.md) `recoverableitemsdeletions`папки).</span><span class="sxs-lookup"><span data-stu-id="e6eee-105">**Note** You may not be able to delete items in the recoverable items deletions folder (represented by the [well-known folder name](../resources/mailfolder.md) `recoverableitemsdeletions`).</span></span> <span data-ttu-id="e6eee-106">Дополнительные сведения см. в статье [Хранение удаленных](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) элементов и [Очистка удаленных элементов](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) .</span><span class="sxs-lookup"><span data-stu-id="e6eee-106">See [Deleted item retention](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) and [Clean up deleted items](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) for more information.</span></span>

## <a name="permissions"></a><span data-ttu-id="e6eee-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="e6eee-107">Permissions</span></span>
<span data-ttu-id="e6eee-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e6eee-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e6eee-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="e6eee-110">Permission type</span></span>      | <span data-ttu-id="e6eee-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="e6eee-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e6eee-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="e6eee-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e6eee-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e6eee-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="e6eee-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="e6eee-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e6eee-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e6eee-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="e6eee-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="e6eee-116">Application</span></span> | <span data-ttu-id="e6eee-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e6eee-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="e6eee-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="e6eee-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}
DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="e6eee-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="e6eee-119">Request headers</span></span>
| <span data-ttu-id="e6eee-120">Имя</span><span class="sxs-lookup"><span data-stu-id="e6eee-120">Name</span></span>       | <span data-ttu-id="e6eee-121">Тип</span><span class="sxs-lookup"><span data-stu-id="e6eee-121">Type</span></span> | <span data-ttu-id="e6eee-122">Описание</span><span class="sxs-lookup"><span data-stu-id="e6eee-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e6eee-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e6eee-123">Authorization</span></span>  | <span data-ttu-id="e6eee-124">string</span><span class="sxs-lookup"><span data-stu-id="e6eee-124">string</span></span>  | <span data-ttu-id="e6eee-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e6eee-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e6eee-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="e6eee-127">Request body</span></span>
<span data-ttu-id="e6eee-128">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="e6eee-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e6eee-129">Ответ</span><span class="sxs-lookup"><span data-stu-id="e6eee-129">Response</span></span>

<span data-ttu-id="e6eee-p104">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="e6eee-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e6eee-132">Пример</span><span class="sxs-lookup"><span data-stu-id="e6eee-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e6eee-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="e6eee-133">Request</span></span>
<span data-ttu-id="e6eee-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="e6eee-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_message"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="e6eee-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="e6eee-135">Response</span></span>
<span data-ttu-id="e6eee-136">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="e6eee-136">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="e6eee-137">Пример кода для SDK</span><span class="sxs-lookup"><span data-stu-id="e6eee-137">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="e6eee-138">Языках</span><span class="sxs-lookup"><span data-stu-id="e6eee-138">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/delete_message-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="e6eee-139">Язык</span><span class="sxs-lookup"><span data-stu-id="e6eee-139">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/delete_message-Javascript-snippets.md)]

---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete message",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/v1.0/api/message-delete.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/v1.0/api/message-delete.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}-->
