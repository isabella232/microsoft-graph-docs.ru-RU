---
title: 'TableColumn: HeaderRowRange'
description: Получает объект диапазона, связанный со строкой заголовков столбца.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 04246fc4b65b587ab20d8e4810c36e7ba5b08c14
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35886587"
---
# <a name="tablecolumn-headerrowrange"></a><span data-ttu-id="8d8ef-103">TableColumn: HeaderRowRange</span><span class="sxs-lookup"><span data-stu-id="8d8ef-103">TableColumn: HeaderRowRange</span></span>

<span data-ttu-id="8d8ef-104">Получает объект диапазона, связанный со строкой заголовков столбца.</span><span class="sxs-lookup"><span data-stu-id="8d8ef-104">Gets the range object associated with the header row of the column.</span></span>
## <a name="permissions"></a><span data-ttu-id="8d8ef-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="8d8ef-105">Permissions</span></span>
<span data-ttu-id="8d8ef-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8d8ef-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8d8ef-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="8d8ef-108">Permission type</span></span>      | <span data-ttu-id="8d8ef-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="8d8ef-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8d8ef-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8d8ef-110">Delegated (work or school account)</span></span> | <span data-ttu-id="8d8ef-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8d8ef-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="8d8ef-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="8d8ef-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8d8ef-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8d8ef-113">Not supported.</span></span>    |
|<span data-ttu-id="8d8ef-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="8d8ef-114">Application</span></span> | <span data-ttu-id="8d8ef-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8d8ef-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8d8ef-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="8d8ef-116">HTTP request</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="8d8ef-117">HTTP</span><span class="sxs-lookup"><span data-stu-id="8d8ef-117">HTTP</span></span>](#tab/http)
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/headerRowRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/headerRowRange

```
## <a name="request-headers"></a><span data-ttu-id="8d8ef-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="8d8ef-118">Request headers</span></span>
| <span data-ttu-id="8d8ef-119">Имя</span><span class="sxs-lookup"><span data-stu-id="8d8ef-119">Name</span></span>       | <span data-ttu-id="8d8ef-120">Описание</span><span class="sxs-lookup"><span data-stu-id="8d8ef-120">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="8d8ef-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="8d8ef-121">Authorization</span></span>  | <span data-ttu-id="8d8ef-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="8d8ef-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8d8ef-124">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="8d8ef-124">Workbook-Session-Id</span></span>  | <span data-ttu-id="8d8ef-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="8d8ef-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="8d8ef-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="8d8ef-127">Request body</span></span>

## <a name="response"></a><span data-ttu-id="8d8ef-128">Отклик</span><span class="sxs-lookup"><span data-stu-id="8d8ef-128">Response</span></span>

<span data-ttu-id="8d8ef-129">В случае успеха этот метод возвращает код отклика `200 OK` и объект [Range](../resources/range.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="8d8ef-129">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8d8ef-130">Пример</span><span class="sxs-lookup"><span data-stu-id="8d8ef-130">Example</span></span>
<span data-ttu-id="8d8ef-131">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="8d8ef-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="8d8ef-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="8d8ef-132">Request</span></span>
<span data-ttu-id="8d8ef-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="8d8ef-133">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "tablecolumn_headerrowrange",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/headerRowRange
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="8d8ef-134">C#</span><span class="sxs-lookup"><span data-stu-id="8d8ef-134">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/tablecolumn-headerrowrange-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="8d8ef-135">Javascript</span><span class="sxs-lookup"><span data-stu-id="8d8ef-135">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/tablecolumn-headerrowrange-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="8d8ef-136">Цель — C</span><span class="sxs-lookup"><span data-stu-id="8d8ef-136">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/tablecolumn-headerrowrange-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="8d8ef-137">Java</span><span class="sxs-lookup"><span data-stu-id="8d8ef-137">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/tablecolumn-headerrowrange-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="8d8ef-138">Отклик</span><span class="sxs-lookup"><span data-stu-id="8d8ef-138">Response</span></span>
<span data-ttu-id="8d8ef-p104">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="8d8ef-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableColumn: HeaderRowRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
