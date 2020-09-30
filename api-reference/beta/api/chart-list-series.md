---
title: Список рядов
description: Получение списка объектов chartseries.
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: apiPageType
ms.openlocfilehash: d65eb0ace97fd7a51811df97003ecfa2c5e4e068
ms.sourcegitcommit: a9f0fde9924ad184d315bb2de43c2610002409f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2020
ms.locfileid: "48313032"
---
# <a name="list-series"></a><span data-ttu-id="0654c-103">Список рядов</span><span class="sxs-lookup"><span data-stu-id="0654c-103">List series</span></span>

<span data-ttu-id="0654c-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="0654c-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="0654c-105">Получение списка объектов chartseries.</span><span class="sxs-lookup"><span data-stu-id="0654c-105">Retrieve a list of chartseries objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="0654c-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="0654c-106">Permissions</span></span>
<span data-ttu-id="0654c-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0654c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0654c-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="0654c-109">Permission type</span></span>      | <span data-ttu-id="0654c-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="0654c-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0654c-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="0654c-111">Delegated (work or school account)</span></span> | <span data-ttu-id="0654c-112">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0654c-112">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0654c-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="0654c-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0654c-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0654c-114">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0654c-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="0654c-115">Application</span></span> | <span data-ttu-id="0654c-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0654c-116">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0654c-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="0654c-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts/{name}/series
```
## <a name="optional-query-parameters"></a><span data-ttu-id="0654c-118">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="0654c-118">Optional query parameters</span></span>
<span data-ttu-id="0654c-119">Этот метод поддерживает [параметры запросов OData](/graph/query-parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="0654c-119">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0654c-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="0654c-120">Request headers</span></span>
| <span data-ttu-id="0654c-121">Имя</span><span class="sxs-lookup"><span data-stu-id="0654c-121">Name</span></span>      |<span data-ttu-id="0654c-122">Описание</span><span class="sxs-lookup"><span data-stu-id="0654c-122">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="0654c-123">Авторизация</span><span class="sxs-lookup"><span data-stu-id="0654c-123">Authorization</span></span>  | <span data-ttu-id="0654c-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="0654c-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0654c-126">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0654c-126">Workbook-Session-Id</span></span>  | <span data-ttu-id="0654c-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="0654c-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0654c-129">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="0654c-129">Request body</span></span>
<span data-ttu-id="0654c-130">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="0654c-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0654c-131">Отклик</span><span class="sxs-lookup"><span data-stu-id="0654c-131">Response</span></span>

<span data-ttu-id="0654c-132">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и коллекцию объектов [воркбукчартсериес](../resources/workbookchartseries.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="0654c-132">If successful, this method returns a `200 OK` response code and collection of [workbookChartSeries](../resources/workbookchartseries.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0654c-133">Пример</span><span class="sxs-lookup"><span data-stu-id="0654c-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0654c-134">Запрос</span><span class="sxs-lookup"><span data-stu-id="0654c-134">Request</span></span>
<span data-ttu-id="0654c-135">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="0654c-135">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="0654c-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="0654c-136">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_series"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series
```
# <a name="c"></a>[<span data-ttu-id="0654c-137">C#</span><span class="sxs-lookup"><span data-stu-id="0654c-137">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-series-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="0654c-138">JavaScript</span><span class="sxs-lookup"><span data-stu-id="0654c-138">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-series-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="0654c-139">Objective-C</span><span class="sxs-lookup"><span data-stu-id="0654c-139">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-series-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="0654c-140">Отклик</span><span class="sxs-lookup"><span data-stu-id="0654c-140">Response</span></span>
<span data-ttu-id="0654c-p104">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="0654c-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartSeries",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 59

{
  "value": [
    {
      "name": "name-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "List series",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->