---
title: 'Range: LastCell'
description: .
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: ea038260af6596c349f00a15e047d6f7eb0b74fb
ms.sourcegitcommit: 0e1101d499f35b08aa2309e273871438b1774979
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2019
ms.locfileid: "35265571"
---
# <a name="range-lastcell"></a><span data-ttu-id="d9d8c-103">Range: LastCell</span><span class="sxs-lookup"><span data-stu-id="d9d8c-103">Range: LastCell</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="d9d8c-p101">Возвращает последнюю ячейку в диапазоне. Например, последняя ячейка диапазона B2:D5 — D5.</span><span class="sxs-lookup"><span data-stu-id="d9d8c-p101">Gets the last cell within the range. For example, the last cell of "B2:D5" is "D5".</span></span>
## <a name="permissions"></a><span data-ttu-id="d9d8c-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="d9d8c-106">Permissions</span></span>
<span data-ttu-id="d9d8c-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d9d8c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d9d8c-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="d9d8c-109">Permission type</span></span>      | <span data-ttu-id="d9d8c-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="d9d8c-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d9d8c-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d9d8c-111">Delegated (work or school account)</span></span> | <span data-ttu-id="d9d8c-112">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9d8c-112">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d9d8c-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="d9d8c-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d9d8c-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9d8c-114">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d9d8c-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="d9d8c-115">Application</span></span> | <span data-ttu-id="d9d8c-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d9d8c-116">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d9d8c-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="d9d8c-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/LastCell
GET /workbook/worksheets/{id|name}/range(address='<address>')/LastCell
GET /workbook/tables/{id|name}/columns/{id|name}/range/LastCell

```
## <a name="request-headers"></a><span data-ttu-id="d9d8c-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="d9d8c-118">Request headers</span></span>
| <span data-ttu-id="d9d8c-119">Имя</span><span class="sxs-lookup"><span data-stu-id="d9d8c-119">Name</span></span>       | <span data-ttu-id="d9d8c-120">Описание</span><span class="sxs-lookup"><span data-stu-id="d9d8c-120">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d9d8c-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="d9d8c-121">Authorization</span></span>  | <span data-ttu-id="d9d8c-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d9d8c-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d9d8c-124">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d9d8c-124">Workbook-Session-Id</span></span>  | <span data-ttu-id="d9d8c-p104">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="d9d8c-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d9d8c-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="d9d8c-127">Request body</span></span>

## <a name="response"></a><span data-ttu-id="d9d8c-128">Отклик</span><span class="sxs-lookup"><span data-stu-id="d9d8c-128">Response</span></span>

<span data-ttu-id="d9d8c-129">В случае успеха этот метод возвращает код отклика `200 OK` и объект [workbookRange](../resources/workbookrange.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="d9d8c-129">If successful, this method returns `200 OK` response code and [workbookRange](../resources/workbookrange.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d9d8c-130">Пример</span><span class="sxs-lookup"><span data-stu-id="d9d8c-130">Example</span></span>
<span data-ttu-id="d9d8c-131">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="d9d8c-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d9d8c-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="d9d8c-132">Request</span></span>
<span data-ttu-id="d9d8c-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="d9d8c-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_lastcell"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names/{name}/range/LastCell
```

##### <a name="response"></a><span data-ttu-id="d9d8c-134">Отклик</span><span class="sxs-lookup"><span data-stu-id="d9d8c-134">Response</span></span>
<span data-ttu-id="d9d8c-p105">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="d9d8c-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
#### <a name="sdk-sample-code"></a><span data-ttu-id="d9d8c-138">Пример кода SDK</span><span class="sxs-lookup"><span data-stu-id="d9d8c-138">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="d9d8c-139">C#</span><span class="sxs-lookup"><span data-stu-id="d9d8c-139">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/range_lastcell-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="d9d8c-140">Javascript</span><span class="sxs-lookup"><span data-stu-id="d9d8c-140">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/range_lastcell-Javascript-snippets.md)]

# <a name="objective-ctabobjective-c"></a>[<span data-ttu-id="d9d8c-141">Цель — C</span><span class="sxs-lookup"><span data-stu-id="d9d8c-141">Objective-C</span></span>](#tab/objective-c)
[!INCLUDE [sample-code](../includes/range_lastcell-Objective-C-snippets.md)]
---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Range: LastCell",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/range-lastcell.md:\r\n      BookmarkMissing: '[#tab/objective-c](Objective-C)'. Did you mean: #objective-c (score: 4)",
    "Error: /api-reference/beta/api/range-lastcell.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/beta/api/range-lastcell.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}
-->
