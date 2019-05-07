---
title: Удаление объекта eventMessage
description: Удаление объекта eventMessage.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 5e5c2c098b0031d3e130a1185b89e9e88d5683b8
ms.sourcegitcommit: b8d01acfc1cb7610a0e1f5c18065da415bae0777
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2019
ms.locfileid: "33615132"
---
# <a name="delete-eventmessage"></a><span data-ttu-id="a21fe-103">Удаление объекта eventMessage</span><span class="sxs-lookup"><span data-stu-id="a21fe-103">Delete eventMessage</span></span>

<span data-ttu-id="a21fe-104">Удаление объекта eventMessage.</span><span class="sxs-lookup"><span data-stu-id="a21fe-104">Delete eventMessage.</span></span>
## <a name="permissions"></a><span data-ttu-id="a21fe-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="a21fe-105">Permissions</span></span>
<span data-ttu-id="a21fe-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a21fe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a21fe-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="a21fe-108">Permission type</span></span>      | <span data-ttu-id="a21fe-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="a21fe-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a21fe-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a21fe-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a21fe-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a21fe-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="a21fe-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="a21fe-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a21fe-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a21fe-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="a21fe-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="a21fe-114">Application</span></span> | <span data-ttu-id="a21fe-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a21fe-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="a21fe-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="a21fe-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}

DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="a21fe-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="a21fe-117">Request headers</span></span>
| <span data-ttu-id="a21fe-118">Имя</span><span class="sxs-lookup"><span data-stu-id="a21fe-118">Name</span></span>       | <span data-ttu-id="a21fe-119">Тип</span><span class="sxs-lookup"><span data-stu-id="a21fe-119">Type</span></span> | <span data-ttu-id="a21fe-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a21fe-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="a21fe-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a21fe-121">Authorization</span></span>  | <span data-ttu-id="a21fe-122">string</span><span class="sxs-lookup"><span data-stu-id="a21fe-122">string</span></span>  | <span data-ttu-id="a21fe-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a21fe-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a21fe-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="a21fe-125">Request body</span></span>
<span data-ttu-id="a21fe-126">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="a21fe-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a21fe-127">Ответ</span><span class="sxs-lookup"><span data-stu-id="a21fe-127">Response</span></span>

<span data-ttu-id="a21fe-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="a21fe-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a21fe-130">Пример</span><span class="sxs-lookup"><span data-stu-id="a21fe-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a21fe-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="a21fe-131">Request</span></span>
<span data-ttu-id="a21fe-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="a21fe-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_eventmessage"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="a21fe-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="a21fe-133">Response</span></span>
<span data-ttu-id="a21fe-134">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="a21fe-134">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="a21fe-135">Пример кода для SDK</span><span class="sxs-lookup"><span data-stu-id="a21fe-135">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="a21fe-136">Языках</span><span class="sxs-lookup"><span data-stu-id="a21fe-136">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/delete_eventmessage-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="a21fe-137">Язык</span><span class="sxs-lookup"><span data-stu-id="a21fe-137">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/delete_eventmessage-Javascript-snippets.md)]

---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete eventMessage",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/v1.0/api/eventmessage-delete.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/v1.0/api/eventmessage-delete.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}-->
