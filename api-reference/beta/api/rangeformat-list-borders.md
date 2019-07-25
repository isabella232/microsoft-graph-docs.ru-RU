---
title: Список границ
description: Получение списка объектов rangeborder.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 5b22c7aaf3019a681609aba104a18dd94f7c2720
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35874396"
---
# <a name="list-borders"></a><span data-ttu-id="dac29-103">Список границ</span><span class="sxs-lookup"><span data-stu-id="dac29-103">List borders</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="dac29-104">Получение списка объектов rangeborder.</span><span class="sxs-lookup"><span data-stu-id="dac29-104">Retrieve a list of rangeborder objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="dac29-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="dac29-105">Permissions</span></span>
<span data-ttu-id="dac29-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dac29-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dac29-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="dac29-108">Permission type</span></span>      | <span data-ttu-id="dac29-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="dac29-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dac29-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="dac29-110">Delegated (work or school account)</span></span> | <span data-ttu-id="dac29-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dac29-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="dac29-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="dac29-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dac29-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dac29-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="dac29-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="dac29-114">Application</span></span> | <span data-ttu-id="dac29-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dac29-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dac29-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="dac29-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/format/borders
GET /workbook/worksheets/{id|name}/range(address='<address>')/format/borders
GET /workbook/tables/{id|name}/columns/{id|name}/range/format/borders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="dac29-117">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="dac29-117">Optional query parameters</span></span>
<span data-ttu-id="dac29-118">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="dac29-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="dac29-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="dac29-119">Request headers</span></span>
| <span data-ttu-id="dac29-120">Имя</span><span class="sxs-lookup"><span data-stu-id="dac29-120">Name</span></span>      |<span data-ttu-id="dac29-121">Описание</span><span class="sxs-lookup"><span data-stu-id="dac29-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="dac29-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="dac29-122">Authorization</span></span>  | <span data-ttu-id="dac29-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="dac29-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="dac29-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="dac29-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="dac29-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="dac29-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="dac29-128">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="dac29-128">Request body</span></span>
<span data-ttu-id="dac29-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="dac29-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dac29-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="dac29-130">Response</span></span>

<span data-ttu-id="dac29-131">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и коллекцию объектов [воркбукранжебордер](../resources/workbookrangeborder.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="dac29-131">If successful, this method returns a `200 OK` response code and collection of [workbookRangeBorder](../resources/workbookrangeborder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="dac29-132">Пример</span><span class="sxs-lookup"><span data-stu-id="dac29-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dac29-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="dac29-133">Request</span></span>
<span data-ttu-id="dac29-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="dac29-134">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="dac29-135">HTTP</span><span class="sxs-lookup"><span data-stu-id="dac29-135">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_borders"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names/{name}/range/format/borders
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="dac29-136">C#</span><span class="sxs-lookup"><span data-stu-id="dac29-136">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-borders-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="dac29-137">Javascript</span><span class="sxs-lookup"><span data-stu-id="dac29-137">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-borders-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="dac29-138">Цель — C</span><span class="sxs-lookup"><span data-stu-id="dac29-138">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-borders-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="dac29-139">Java</span><span class="sxs-lookup"><span data-stu-id="dac29-139">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-borders-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="dac29-140">Отклик</span><span class="sxs-lookup"><span data-stu-id="dac29-140">Response</span></span>
<span data-ttu-id="dac29-p104">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="dac29-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeBorder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 185

{
  "value": [
    {
      "id": "id-value",
      "color": "color-value",
      "style": "style-value",
      "sideIndex": "sideIndex-value",
      "weight": "weight-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "List borders",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
