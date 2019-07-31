---
title: Close Session
description: 'Используйте этот API для закрытия существующего сеанса книги. '
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: apiPageType
ms.openlocfilehash: 1fea58a37b5cf4747965726442e91070542a9e15
ms.sourcegitcommit: 2c62457e57467b8d50f21b255b553106a9a5d8d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2019
ms.locfileid: "35996114"
---
# <a name="close-session"></a><span data-ttu-id="a0304-103">Close Session</span><span class="sxs-lookup"><span data-stu-id="a0304-103">Close Session</span></span>

<span data-ttu-id="a0304-104">Используйте этот API для закрытия существующего сеанса книги.</span><span class="sxs-lookup"><span data-stu-id="a0304-104">Use this API to close an existing workbook session.</span></span> 

## <a name="permissions"></a><span data-ttu-id="a0304-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="a0304-105">Permissions</span></span>
<span data-ttu-id="a0304-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a0304-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a0304-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="a0304-108">Permission type</span></span>      | <span data-ttu-id="a0304-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="a0304-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a0304-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a0304-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a0304-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a0304-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a0304-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="a0304-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a0304-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a0304-113">Not supported.</span></span>    |
|<span data-ttu-id="a0304-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="a0304-114">Application</span></span> | <span data-ttu-id="a0304-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a0304-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a0304-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="a0304-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/closeSession
workbook-session-id: {session-id}
```
## <a name="request-headers"></a><span data-ttu-id="a0304-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="a0304-117">Request headers</span></span>
| <span data-ttu-id="a0304-118">Имя</span><span class="sxs-lookup"><span data-stu-id="a0304-118">Name</span></span>       | <span data-ttu-id="a0304-119">Описание</span><span class="sxs-lookup"><span data-stu-id="a0304-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a0304-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="a0304-120">Authorization</span></span>  | <span data-ttu-id="a0304-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a0304-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a0304-123">workbook-session-id</span><span class="sxs-lookup"><span data-stu-id="a0304-123">workbook-session-id</span></span> | <span data-ttu-id="a0304-124">Идентификатор сеанса книги, которую необходимо закрыть</span><span class="sxs-lookup"><span data-stu-id="a0304-124">Workbook session Id to be closed</span></span> |

## <a name="request-body"></a><span data-ttu-id="a0304-125">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="a0304-125">Request body</span></span>
<span data-ttu-id="a0304-126">Для этого API не нужно тело запроса.</span><span class="sxs-lookup"><span data-stu-id="a0304-126">This API does not require any request body.</span></span>

## <a name="response"></a><span data-ttu-id="a0304-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="a0304-127">Response</span></span>

<span data-ttu-id="a0304-128">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="a0304-128">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="a0304-129">Пример</span><span class="sxs-lookup"><span data-stu-id="a0304-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a0304-130">Запрос</span><span class="sxs-lookup"><span data-stu-id="a0304-130">Request</span></span>
<span data-ttu-id="a0304-131">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="a0304-131">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="a0304-132">HTTP</span><span class="sxs-lookup"><span data-stu-id="a0304-132">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "close_excel_session"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/closeSession
Content-type: application/json
workbook-session-id: {session-id}
Content-length: 0

{

}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="a0304-133">C#</span><span class="sxs-lookup"><span data-stu-id="a0304-133">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/close-excel-session-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="a0304-134">Javascript</span><span class="sxs-lookup"><span data-stu-id="a0304-134">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/close-excel-session-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="a0304-135">Цель — C</span><span class="sxs-lookup"><span data-stu-id="a0304-135">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/close-excel-session-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="a0304-136">Java</span><span class="sxs-lookup"><span data-stu-id="a0304-136">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/close-excel-session-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


<span data-ttu-id="a0304-137">Обратите внимание, что заголовок workbook-session-id является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a0304-137">Note that workbook-session-id header is required.</span></span> 


##### <a name="response"></a><span data-ttu-id="a0304-138">Ответ</span><span class="sxs-lookup"><span data-stu-id="a0304-138">Response</span></span>
<span data-ttu-id="a0304-139">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="a0304-139">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79 
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Example",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
