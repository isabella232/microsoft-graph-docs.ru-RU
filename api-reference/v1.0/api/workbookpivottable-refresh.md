---
title: 'workbookPivotTable: refresh'
description: Обновляет сводную таблицу.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 2674e3f060a90704280f50d7b9202075accb0ab6
ms.sourcegitcommit: b8d01acfc1cb7610a0e1f5c18065da415bae0777
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2019
ms.locfileid: "33600643"
---
# <a name="workbookpivottable-refresh"></a><span data-ttu-id="c8395-103">workbookPivotTable: refresh</span><span class="sxs-lookup"><span data-stu-id="c8395-103">workbookPivotTable: refresh</span></span>

<span data-ttu-id="c8395-104">Обновляет сводную таблицу.</span><span class="sxs-lookup"><span data-stu-id="c8395-104">Refreshes the PivotTable.</span></span>


## <a name="permissions"></a><span data-ttu-id="c8395-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="c8395-105">Permissions</span></span>
<span data-ttu-id="c8395-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c8395-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c8395-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="c8395-108">Permission type</span></span>      | <span data-ttu-id="c8395-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="c8395-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c8395-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c8395-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c8395-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c8395-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c8395-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="c8395-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c8395-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c8395-113">Not supported.</span></span>    |
|<span data-ttu-id="c8395-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="c8395-114">Application</span></span> | <span data-ttu-id="c8395-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c8395-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c8395-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="c8395-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/pivotTables/{id}/refresh
```
## <a name="request-headers"></a><span data-ttu-id="c8395-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="c8395-117">Request headers</span></span>
| <span data-ttu-id="c8395-118">Имя</span><span class="sxs-lookup"><span data-stu-id="c8395-118">Name</span></span>       | <span data-ttu-id="c8395-119">Описание</span><span class="sxs-lookup"><span data-stu-id="c8395-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c8395-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="c8395-120">Authorization</span></span>  | <span data-ttu-id="c8395-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="c8395-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c8395-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c8395-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="c8395-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="c8395-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c8395-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="c8395-126">Request body</span></span>

### <a name="response"></a><span data-ttu-id="c8395-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="c8395-127">Response</span></span>
<span data-ttu-id="c8395-p104">В случае успешного выполнения этот метод возвращает код отклика `200 OK`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="c8395-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c8395-130">Пример</span><span class="sxs-lookup"><span data-stu-id="c8395-130">Example</span></span>
<span data-ttu-id="c8395-131">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="c8395-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c8395-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="c8395-132">Request</span></span>
<span data-ttu-id="c8395-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="c8395-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookpivottable_refresh"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/pivotTables/{id}/refresh
```

##### <a name="response"></a><span data-ttu-id="c8395-134">Отклик</span><span class="sxs-lookup"><span data-stu-id="c8395-134">Response</span></span>
<span data-ttu-id="c8395-135">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="c8395-135">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="c8395-136">Пример кода для SDK</span><span class="sxs-lookup"><span data-stu-id="c8395-136">SDK sample code</span></span>

# <a name="ctabcs"></a>[<span data-ttu-id="c8395-137">Языках</span><span class="sxs-lookup"><span data-stu-id="c8395-137">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/workbookpivottable_refresh-Cs-snippets.md)]

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
    "Error: /api-reference/v1.0/api/workbookpivottable-refresh.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/v1.0/api/workbookpivottable-refresh.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}-->
