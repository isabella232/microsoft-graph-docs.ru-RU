---
title: 'Range: delete'
description: Удаляет ячейки, связанные с диапазоном.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: cd55c7abb6cb60cfe9ff6080fcf28a75f65d4257
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35857121"
---
# <a name="range-delete"></a><span data-ttu-id="f3dde-103">Range: delete</span><span class="sxs-lookup"><span data-stu-id="f3dde-103">Range: delete</span></span>

<span data-ttu-id="f3dde-104">Удаляет ячейки, связанные с диапазоном.</span><span class="sxs-lookup"><span data-stu-id="f3dde-104">Deletes the cells associated with the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="f3dde-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="f3dde-105">Permissions</span></span>
<span data-ttu-id="f3dde-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f3dde-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f3dde-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="f3dde-108">Permission type</span></span>      | <span data-ttu-id="f3dde-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="f3dde-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f3dde-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="f3dde-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f3dde-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f3dde-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f3dde-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="f3dde-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f3dde-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f3dde-113">Not supported.</span></span>    |
|<span data-ttu-id="f3dde-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="f3dde-114">Application</span></span> | <span data-ttu-id="f3dde-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f3dde-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f3dde-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="f3dde-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/delete
POST /workbook/worksheets/{id|name}/range(address='<address>')/delete
POST /workbook/tables/{id|name}/columns/{id|name}/range/delete

```
## <a name="request-headers"></a><span data-ttu-id="f3dde-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="f3dde-117">Request headers</span></span>
| <span data-ttu-id="f3dde-118">Имя</span><span class="sxs-lookup"><span data-stu-id="f3dde-118">Name</span></span>       | <span data-ttu-id="f3dde-119">Описание</span><span class="sxs-lookup"><span data-stu-id="f3dde-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f3dde-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="f3dde-120">Authorization</span></span>  | <span data-ttu-id="f3dde-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="f3dde-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f3dde-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f3dde-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="f3dde-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="f3dde-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f3dde-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="f3dde-126">Request body</span></span>
<span data-ttu-id="f3dde-127">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="f3dde-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f3dde-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="f3dde-128">Parameter</span></span>    | <span data-ttu-id="f3dde-129">Тип</span><span class="sxs-lookup"><span data-stu-id="f3dde-129">Type</span></span>   |<span data-ttu-id="f3dde-130">Описание</span><span class="sxs-lookup"><span data-stu-id="f3dde-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f3dde-131">shift</span><span class="sxs-lookup"><span data-stu-id="f3dde-131">shift</span></span>|<span data-ttu-id="f3dde-132">string</span><span class="sxs-lookup"><span data-stu-id="f3dde-132">string</span></span>|<span data-ttu-id="f3dde-133">Определяет способ сдвига ячеек.</span><span class="sxs-lookup"><span data-stu-id="f3dde-133">Specifies which way to shift the cells.</span></span>  <span data-ttu-id="f3dde-134">Возможные значения: `Up`, `Left`.</span><span class="sxs-lookup"><span data-stu-id="f3dde-134">The possible values are: `Up`, `Left`.</span></span>|

## <a name="response"></a><span data-ttu-id="f3dde-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="f3dde-135">Response</span></span>

<span data-ttu-id="f3dde-p105">В случае успешного выполнения этот метод возвращает код отклика `200 OK`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="f3dde-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f3dde-138">Пример</span><span class="sxs-lookup"><span data-stu-id="f3dde-138">Example</span></span>
<span data-ttu-id="f3dde-139">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="f3dde-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f3dde-140">Запрос</span><span class="sxs-lookup"><span data-stu-id="f3dde-140">Request</span></span>
<span data-ttu-id="f3dde-141">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="f3dde-141">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="f3dde-142">HTTP</span><span class="sxs-lookup"><span data-stu-id="f3dde-142">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "range_delete"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/delete
Content-type: application/json
Content-length: 28

{
  "shift": "shift-value"
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="f3dde-143">C#</span><span class="sxs-lookup"><span data-stu-id="f3dde-143">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/range-delete-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="f3dde-144">Javascript</span><span class="sxs-lookup"><span data-stu-id="f3dde-144">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/range-delete-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="f3dde-145">Цель — C</span><span class="sxs-lookup"><span data-stu-id="f3dde-145">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/range-delete-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="f3dde-146">Java</span><span class="sxs-lookup"><span data-stu-id="f3dde-146">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/range-delete-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="f3dde-147">Отклик</span><span class="sxs-lookup"><span data-stu-id="f3dde-147">Response</span></span>
<span data-ttu-id="f3dde-148">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="f3dde-148">Here is an example of the response.</span></span> 
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
  "description": "Range: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
