---
title: 'workbookPivotTable: refresh'
description: Обновляет сводную таблицу.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 3f22136eba56e0086b3dd9d7f74af9d731f7e2e0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35459848"
---
# <a name="workbookpivottable-refresh"></a><span data-ttu-id="5f4f6-103">workbookPivotTable: refresh</span><span class="sxs-lookup"><span data-stu-id="5f4f6-103">workbookPivotTable: refresh</span></span>

<span data-ttu-id="5f4f6-104">Обновляет сводную таблицу.</span><span class="sxs-lookup"><span data-stu-id="5f4f6-104">Refreshes the PivotTable.</span></span>


## <a name="permissions"></a><span data-ttu-id="5f4f6-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="5f4f6-105">Permissions</span></span>
<span data-ttu-id="5f4f6-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5f4f6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="5f4f6-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="5f4f6-108">Permission type</span></span>      | <span data-ttu-id="5f4f6-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="5f4f6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5f4f6-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="5f4f6-110">Delegated (work or school account)</span></span> | <span data-ttu-id="5f4f6-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5f4f6-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="5f4f6-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="5f4f6-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5f4f6-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5f4f6-113">Not supported.</span></span>    |
|<span data-ttu-id="5f4f6-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="5f4f6-114">Application</span></span> | <span data-ttu-id="5f4f6-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5f4f6-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5f4f6-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="5f4f6-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/pivotTables/{id}/refresh
```
## <a name="request-headers"></a><span data-ttu-id="5f4f6-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="5f4f6-117">Request headers</span></span>
| <span data-ttu-id="5f4f6-118">Имя</span><span class="sxs-lookup"><span data-stu-id="5f4f6-118">Name</span></span>       | <span data-ttu-id="5f4f6-119">Описание</span><span class="sxs-lookup"><span data-stu-id="5f4f6-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="5f4f6-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="5f4f6-120">Authorization</span></span>  | <span data-ttu-id="5f4f6-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5f4f6-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5f4f6-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="5f4f6-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="5f4f6-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="5f4f6-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5f4f6-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="5f4f6-126">Request body</span></span>

### <a name="response"></a><span data-ttu-id="5f4f6-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="5f4f6-127">Response</span></span>
<span data-ttu-id="5f4f6-p104">В случае успешного выполнения этот метод возвращает код отклика `200 OK`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="5f4f6-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5f4f6-130">Пример</span><span class="sxs-lookup"><span data-stu-id="5f4f6-130">Example</span></span>
<span data-ttu-id="5f4f6-131">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="5f4f6-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5f4f6-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="5f4f6-132">Request</span></span>
<span data-ttu-id="5f4f6-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="5f4f6-133">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="5f4f6-134">HTTP</span><span class="sxs-lookup"><span data-stu-id="5f4f6-134">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "workbookpivottable_refresh"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/pivotTables/{id}/refresh
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="5f4f6-135">C#</span><span class="sxs-lookup"><span data-stu-id="5f4f6-135">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/workbookpivottable-refresh-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="5f4f6-136">Javascript</span><span class="sxs-lookup"><span data-stu-id="5f4f6-136">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/workbookpivottable-refresh-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="5f4f6-137">Цель — C</span><span class="sxs-lookup"><span data-stu-id="5f4f6-137">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/workbookpivottable-refresh-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="5f4f6-138">Отклик</span><span class="sxs-lookup"><span data-stu-id="5f4f6-138">Response</span></span>
<span data-ttu-id="5f4f6-139">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="5f4f6-139">Here is an example of the response.</span></span>
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
  "description": "Example",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
