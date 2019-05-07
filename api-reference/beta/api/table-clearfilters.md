---
title: 'Table: clearFilters'
description: Очищает все фильтры, примененные к таблице.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 1a35b103c01e0ad6a46be39a4231de63e3dae337
ms.sourcegitcommit: 3e5f4f515f050e16680ec44f68af40583147af9e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2019
ms.locfileid: "33637901"
---
# <a name="table-clearfilters"></a><span data-ttu-id="88c90-103">Table: clearFilters</span><span class="sxs-lookup"><span data-stu-id="88c90-103">Table: clearFilters</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="88c90-104">Очищает все фильтры, примененные к таблице.</span><span class="sxs-lookup"><span data-stu-id="88c90-104">Clears all the filters currently applied on the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="88c90-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="88c90-105">Permissions</span></span>
<span data-ttu-id="88c90-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="88c90-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="88c90-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="88c90-108">Permission type</span></span>      | <span data-ttu-id="88c90-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="88c90-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="88c90-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="88c90-110">Delegated (work or school account)</span></span> | <span data-ttu-id="88c90-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88c90-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="88c90-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="88c90-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="88c90-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88c90-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="88c90-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="88c90-114">Application</span></span> | <span data-ttu-id="88c90-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="88c90-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="88c90-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="88c90-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/clearFilters
POST /workbook/worksheets/{id|name}/tables/{id|name}/clearFilters

```
## <a name="request-headers"></a><span data-ttu-id="88c90-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="88c90-117">Request headers</span></span>
| <span data-ttu-id="88c90-118">Имя</span><span class="sxs-lookup"><span data-stu-id="88c90-118">Name</span></span>       | <span data-ttu-id="88c90-119">Описание</span><span class="sxs-lookup"><span data-stu-id="88c90-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="88c90-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="88c90-120">Authorization</span></span>  | <span data-ttu-id="88c90-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="88c90-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="88c90-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="88c90-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="88c90-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="88c90-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="88c90-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="88c90-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="88c90-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="88c90-127">Response</span></span>

<span data-ttu-id="88c90-p104">В случае успешного выполнения этот метод возвращает код отклика `200 OK`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="88c90-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="88c90-130">Пример</span><span class="sxs-lookup"><span data-stu-id="88c90-130">Example</span></span>
<span data-ttu-id="88c90-131">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="88c90-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="88c90-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="88c90-132">Request</span></span>
<span data-ttu-id="88c90-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="88c90-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_clearfilters"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/clearFilters
```

##### <a name="response"></a><span data-ttu-id="88c90-134">Отклик</span><span class="sxs-lookup"><span data-stu-id="88c90-134">Response</span></span>
<span data-ttu-id="88c90-135">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="88c90-135">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="88c90-136">Пример кода для SDK</span><span class="sxs-lookup"><span data-stu-id="88c90-136">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="88c90-137">Языках</span><span class="sxs-lookup"><span data-stu-id="88c90-137">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/table_clearfilters-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="88c90-138">Язык</span><span class="sxs-lookup"><span data-stu-id="88c90-138">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/table_clearfilters-Javascript-snippets.md)]

---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Table: clearFilters",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/table-clearfilters.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/beta/api/table-clearfilters.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}
-->
