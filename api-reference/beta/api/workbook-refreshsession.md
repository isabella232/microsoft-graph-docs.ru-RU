---
title: Refresh Session
description: 'Используйте этот API для обновления существующего сеанса книги. '
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 0f159951f8198ff2f7822d63d6ef86f7c1fc21a1
ms.sourcegitcommit: 94aaf594c881c02f353c6a417460cdf783a0bfe0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2019
ms.locfileid: "33960942"
---
# <a name="refresh-session"></a><span data-ttu-id="0a237-103">Refresh Session</span><span class="sxs-lookup"><span data-stu-id="0a237-103">Refresh Session</span></span>

<span data-ttu-id="0a237-104">Используйте этот API для обновления существующего сеанса книги.</span><span class="sxs-lookup"><span data-stu-id="0a237-104">Use this API to refresh an existing workbook session.</span></span> 

## <a name="permissions"></a><span data-ttu-id="0a237-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="0a237-105">Permissions</span></span>
<span data-ttu-id="0a237-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0a237-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0a237-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="0a237-108">Permission type</span></span>      | <span data-ttu-id="0a237-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="0a237-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0a237-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="0a237-110">Delegated (work or school account)</span></span> | <span data-ttu-id="0a237-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0a237-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0a237-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="0a237-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0a237-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0a237-113">Not supported.</span></span>    |
|<span data-ttu-id="0a237-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="0a237-114">Application</span></span> | <span data-ttu-id="0a237-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0a237-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0a237-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="0a237-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/refreshSession
workbook-session-id: {session-id}
```
## <a name="request-headers"></a><span data-ttu-id="0a237-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="0a237-117">Request headers</span></span>
| <span data-ttu-id="0a237-118">Имя</span><span class="sxs-lookup"><span data-stu-id="0a237-118">Name</span></span>       | <span data-ttu-id="0a237-119">Описание</span><span class="sxs-lookup"><span data-stu-id="0a237-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0a237-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="0a237-120">Authorization</span></span>  | <span data-ttu-id="0a237-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="0a237-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0a237-123">workbook-session-id</span><span class="sxs-lookup"><span data-stu-id="0a237-123">workbook-session-id</span></span> | <span data-ttu-id="0a237-124">Идентификатор сеанса для книги, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="0a237-124">Workbook session Id to be refreshed</span></span> |

## <a name="request-body"></a><span data-ttu-id="0a237-125">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="0a237-125">Request body</span></span>
<span data-ttu-id="0a237-126">Для этого API не нужно тело запроса.</span><span class="sxs-lookup"><span data-stu-id="0a237-126">This API does not require any request body.</span></span>

## <a name="response"></a><span data-ttu-id="0a237-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="0a237-127">Response</span></span>

<span data-ttu-id="0a237-128">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="0a237-128">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="0a237-129">Пример</span><span class="sxs-lookup"><span data-stu-id="0a237-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0a237-130">Запрос</span><span class="sxs-lookup"><span data-stu-id="0a237-130">Request</span></span>
<span data-ttu-id="0a237-131">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="0a237-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "refresh_excel_session"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/refreshSession
Content-type: application/json
workbook-session-id: {session-id}
Content-length: 0

{

}
```

<span data-ttu-id="0a237-132">Обратите внимание, что заголовок workbook-session-id является обязательным.</span><span class="sxs-lookup"><span data-stu-id="0a237-132">Note that workbook-session-id header is required.</span></span> 


##### <a name="response"></a><span data-ttu-id="0a237-133">Ответ</span><span class="sxs-lookup"><span data-stu-id="0a237-133">Response</span></span>
<span data-ttu-id="0a237-134">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="0a237-134">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="0a237-135">Пример кода SDK</span><span class="sxs-lookup"><span data-stu-id="0a237-135">SDK sample code</span></span>
# <a name="javascripttabjavascript"></a>[<span data-ttu-id="0a237-136">Javascript</span><span class="sxs-lookup"><span data-stu-id="0a237-136">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/refresh_excel_session-Javascript-snippets.md)]

# <a name="ctabcs"></a>[<span data-ttu-id="0a237-137">C#</span><span class="sxs-lookup"><span data-stu-id="0a237-137">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/refresh_excel_session-Cs-snippets.md)]

---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79 
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Example",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/workbook-refreshsession.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/beta/api/workbook-refreshsession.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}-->
