---
title: Получение Воркбукчартаксис
description: Получение свойств и связей объекта Воркбукчартаксис.
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: apiPageType
ms.openlocfilehash: 271a629b4e0a7d108eb09e913cea98f6fd5814c7
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "36317314"
---
# <a name="get-workbookchartaxis"></a><span data-ttu-id="ca6af-103">Получение Воркбукчартаксис</span><span class="sxs-lookup"><span data-stu-id="ca6af-103">Get workbookChartAxis</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="ca6af-104">Получение свойств и связей объекта chartaxis.</span><span class="sxs-lookup"><span data-stu-id="ca6af-104">Retrieve the properties and relationships of chartaxis object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ca6af-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="ca6af-105">Permissions</span></span>
<span data-ttu-id="ca6af-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ca6af-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ca6af-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="ca6af-108">Permission type</span></span>      | <span data-ttu-id="ca6af-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="ca6af-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ca6af-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="ca6af-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ca6af-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ca6af-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ca6af-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="ca6af-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ca6af-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ca6af-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ca6af-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="ca6af-114">Application</span></span> | <span data-ttu-id="ca6af-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ca6af-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ca6af-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="ca6af-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts/{name}/axes/valueaxis
GET /workbook/worksheets/{id|name}/charts/{name}/axes/seriesaxis
GET /workbook/worksheets/{id|name}/charts/{name}/axes/categoryaxis
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ca6af-117">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="ca6af-117">Optional query parameters</span></span>
<span data-ttu-id="ca6af-118">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="ca6af-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ca6af-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="ca6af-119">Request headers</span></span>
| <span data-ttu-id="ca6af-120">Имя</span><span class="sxs-lookup"><span data-stu-id="ca6af-120">Name</span></span>      |<span data-ttu-id="ca6af-121">Описание</span><span class="sxs-lookup"><span data-stu-id="ca6af-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="ca6af-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="ca6af-122">Authorization</span></span>  | <span data-ttu-id="ca6af-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ca6af-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ca6af-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="ca6af-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="ca6af-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="ca6af-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ca6af-128">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="ca6af-128">Request body</span></span>
<span data-ttu-id="ca6af-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="ca6af-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ca6af-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="ca6af-130">Response</span></span>

<span data-ttu-id="ca6af-131">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и объект [воркбукчартаксис](../resources/workbookchartaxis.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="ca6af-131">If successful, this method returns a `200 OK` response code and [workbookChartAxis](../resources/workbookchartaxis.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ca6af-132">Пример</span><span class="sxs-lookup"><span data-stu-id="ca6af-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ca6af-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="ca6af-133">Request</span></span>
<span data-ttu-id="ca6af-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="ca6af-134">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="ca6af-135">HTTP</span><span class="sxs-lookup"><span data-stu-id="ca6af-135">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_chartaxis"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueaxis
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="ca6af-136">C#</span><span class="sxs-lookup"><span data-stu-id="ca6af-136">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-chartaxis-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="ca6af-137">JavaScript</span><span class="sxs-lookup"><span data-stu-id="ca6af-137">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-chartaxis-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="ca6af-138">Цель — C</span><span class="sxs-lookup"><span data-stu-id="ca6af-138">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-chartaxis-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="ca6af-139">Java</span><span class="sxs-lookup"><span data-stu-id="ca6af-139">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-chartaxis-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="ca6af-140">Отклик</span><span class="sxs-lookup"><span data-stu-id="ca6af-140">Response</span></span>
<span data-ttu-id="ca6af-p104">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="ca6af-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartAxis"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 64

{
  "majorUnit": "string",
  "maximum": "string",
  "minimum": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Get ChartAxis",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
