---
title: 'Table: reapplyFilters'
description: Повторно применяет все текущие фильтры к таблице.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: f6fad4177327a951dadf45881ad2e909a5232e9c
ms.sourcegitcommit: 3e5f4f515f050e16680ec44f68af40583147af9e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2019
ms.locfileid: "33637873"
---
# <a name="table-reapplyfilters"></a><span data-ttu-id="6485e-103">Table: reapplyFilters</span><span class="sxs-lookup"><span data-stu-id="6485e-103">Table: reapplyFilters</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="6485e-104">Повторно применяет все текущие фильтры к таблице.</span><span class="sxs-lookup"><span data-stu-id="6485e-104">Reapplies all the filters currently on the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="6485e-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="6485e-105">Permissions</span></span>
<span data-ttu-id="6485e-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6485e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6485e-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="6485e-108">Permission type</span></span>      | <span data-ttu-id="6485e-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="6485e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6485e-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6485e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="6485e-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6485e-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6485e-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="6485e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6485e-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6485e-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6485e-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="6485e-114">Application</span></span> | <span data-ttu-id="6485e-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6485e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6485e-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="6485e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/reapplyFilters
POST /workbook/worksheets/{id|name}/tables/{id|name}/reapplyFilters

```
## <a name="request-headers"></a><span data-ttu-id="6485e-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="6485e-117">Request headers</span></span>
| <span data-ttu-id="6485e-118">Имя</span><span class="sxs-lookup"><span data-stu-id="6485e-118">Name</span></span>       | <span data-ttu-id="6485e-119">Описание</span><span class="sxs-lookup"><span data-stu-id="6485e-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6485e-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="6485e-120">Authorization</span></span>  | <span data-ttu-id="6485e-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6485e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6485e-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6485e-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="6485e-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="6485e-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6485e-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="6485e-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="6485e-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="6485e-127">Response</span></span>

<span data-ttu-id="6485e-p104">В случае успешного выполнения этот метод возвращает код отклика `200 OK`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="6485e-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6485e-130">Пример</span><span class="sxs-lookup"><span data-stu-id="6485e-130">Example</span></span>
<span data-ttu-id="6485e-131">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="6485e-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="6485e-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="6485e-132">Request</span></span>
<span data-ttu-id="6485e-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="6485e-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_reapplyfilters"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/reapplyFilters
```

##### <a name="response"></a><span data-ttu-id="6485e-134">Отклик</span><span class="sxs-lookup"><span data-stu-id="6485e-134">Response</span></span>
<span data-ttu-id="6485e-135">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="6485e-135">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="6485e-136">Пример кода для SDK</span><span class="sxs-lookup"><span data-stu-id="6485e-136">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="6485e-137">Языках</span><span class="sxs-lookup"><span data-stu-id="6485e-137">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/table_reapplyfilters-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="6485e-138">Язык</span><span class="sxs-lookup"><span data-stu-id="6485e-138">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/table_reapplyfilters-Javascript-snippets.md)]

---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Table: reapplyFilters",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/table-reapplyfilters.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/beta/api/table-reapplyfilters.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}
-->
