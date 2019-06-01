---
title: Удаление приложения
description: Удаляет приложение.
author: davidmu1
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 4723234cad9bfd33272c97f3204be70da05d8e97
ms.sourcegitcommit: 33f1cf5b3b79bfba6a06b52d34e558a6ba327d21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/31/2019
ms.locfileid: "34655168"
---
# <a name="delete-application"></a><span data-ttu-id="4fcd4-103">Удаление приложения</span><span class="sxs-lookup"><span data-stu-id="4fcd4-103">Delete application</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="4fcd4-104">Удаляет приложение.</span><span class="sxs-lookup"><span data-stu-id="4fcd4-104">Deletes an application.</span></span>

## <a name="permissions"></a><span data-ttu-id="4fcd4-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4fcd4-105">Permissions</span></span>
<span data-ttu-id="4fcd4-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4fcd4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4fcd4-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="4fcd4-108">Permission type</span></span>      | <span data-ttu-id="4fcd4-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="4fcd4-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4fcd4-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="4fcd4-110">Delegated (work or school account)</span></span> | <span data-ttu-id="4fcd4-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4fcd4-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4fcd4-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="4fcd4-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4fcd4-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4fcd4-113">Not supported.</span></span>    |
|<span data-ttu-id="4fcd4-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="4fcd4-114">Application</span></span> | <span data-ttu-id="4fcd4-115">Application.ReadWrite.OwnedBy, Application.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4fcd4-115">Application.ReadWrite.OwnedBy, Application.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4fcd4-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="4fcd4-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /applications/{id}
```

## <a name="request-headers"></a><span data-ttu-id="4fcd4-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="4fcd4-117">Request headers</span></span>
| <span data-ttu-id="4fcd4-118">Имя</span><span class="sxs-lookup"><span data-stu-id="4fcd4-118">Name</span></span>       | <span data-ttu-id="4fcd4-119">Тип</span><span class="sxs-lookup"><span data-stu-id="4fcd4-119">Type</span></span> | <span data-ttu-id="4fcd4-120">Описание</span><span class="sxs-lookup"><span data-stu-id="4fcd4-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4fcd4-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="4fcd4-121">Authorization</span></span>  | <span data-ttu-id="4fcd4-122">string</span><span class="sxs-lookup"><span data-stu-id="4fcd4-122">string</span></span>  | <span data-ttu-id="4fcd4-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4fcd4-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4fcd4-125">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="4fcd4-125">Request body</span></span>
<span data-ttu-id="4fcd4-126">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="4fcd4-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4fcd4-127">Ответ</span><span class="sxs-lookup"><span data-stu-id="4fcd4-127">Response</span></span>

<span data-ttu-id="4fcd4-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="4fcd4-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4fcd4-130">Пример</span><span class="sxs-lookup"><span data-stu-id="4fcd4-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4fcd4-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="4fcd4-131">Request</span></span>
<span data-ttu-id="4fcd4-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="4fcd4-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_application"
}-->
```http
DELETE https://graph.microsoft.com/beta/applications/{id}
```
##### <a name="response"></a><span data-ttu-id="4fcd4-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="4fcd4-133">Response</span></span>
<span data-ttu-id="4fcd4-134">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="4fcd4-134">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="4fcd4-135">Пример кода SDK</span><span class="sxs-lookup"><span data-stu-id="4fcd4-135">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="4fcd4-136">C#</span><span class="sxs-lookup"><span data-stu-id="4fcd4-136">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/delete_application-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="4fcd4-137">Javascript</span><span class="sxs-lookup"><span data-stu-id="4fcd4-137">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/delete_application-Javascript-snippets.md)]

---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Delete application",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/application-delete.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/beta/api/application-delete.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}
-->
