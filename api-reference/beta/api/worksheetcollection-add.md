---
title: 'WorksheetCollection: add'
description: . Активируйте ().
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: apiPageType
ms.openlocfilehash: dd758166bf2faf17d0f321b34b2e25f4e88c4e07
ms.sourcegitcommit: 1066aa4045d48f9c9b764d3b2891cf4f806d17d5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2019
ms.locfileid: "36420933"
---
# <a name="worksheetcollection-add"></a><span data-ttu-id="2901b-103">WorksheetCollection: add</span><span class="sxs-lookup"><span data-stu-id="2901b-103">WorksheetCollection: add</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="2901b-p101">Добавляет новый лист в книгу. Лист будет добавлен в конец набора имеющихся листов. Если вы хотите активировать только что добавленный лист, вызовите команду .activate().</span><span class="sxs-lookup"><span data-stu-id="2901b-p101">Adds a new worksheet to the workbook. The worksheet will be added at the end of existing worksheets. If you wish to activate the newly added worksheet, call ".activate() on it.</span></span>
## <a name="permissions"></a><span data-ttu-id="2901b-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="2901b-107">Permissions</span></span>
<span data-ttu-id="2901b-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2901b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2901b-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="2901b-110">Permission type</span></span>      | <span data-ttu-id="2901b-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="2901b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2901b-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="2901b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="2901b-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2901b-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2901b-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="2901b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2901b-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2901b-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2901b-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="2901b-116">Application</span></span> | <span data-ttu-id="2901b-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2901b-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2901b-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="2901b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/

```
## <a name="request-headers"></a><span data-ttu-id="2901b-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="2901b-119">Request headers</span></span>
| <span data-ttu-id="2901b-120">Имя</span><span class="sxs-lookup"><span data-stu-id="2901b-120">Name</span></span>       | <span data-ttu-id="2901b-121">Описание</span><span class="sxs-lookup"><span data-stu-id="2901b-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2901b-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="2901b-122">Authorization</span></span>  | <span data-ttu-id="2901b-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="2901b-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2901b-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="2901b-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="2901b-p104">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="2901b-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2901b-128">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="2901b-128">Request body</span></span>
<span data-ttu-id="2901b-129">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="2901b-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2901b-130">Параметр</span><span class="sxs-lookup"><span data-stu-id="2901b-130">Parameter</span></span>    | <span data-ttu-id="2901b-131">Тип</span><span class="sxs-lookup"><span data-stu-id="2901b-131">Type</span></span>   |<span data-ttu-id="2901b-132">Описание</span><span class="sxs-lookup"><span data-stu-id="2901b-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2901b-133">name</span><span class="sxs-lookup"><span data-stu-id="2901b-133">name</span></span>|<span data-ttu-id="2901b-134">string</span><span class="sxs-lookup"><span data-stu-id="2901b-134">string</span></span>|<span data-ttu-id="2901b-p105">Необязательный параметр. Имя добавляемого листа. Если параметр используется, имя должно быть уникальным. В противном случае Excel определяет имя нового листа.</span><span class="sxs-lookup"><span data-stu-id="2901b-p105">Optional. The name of the worksheet to be added. If specified, name should be unqiue. If not specified, Excel determines the name of the new worksheet.</span></span>|

## <a name="response"></a><span data-ttu-id="2901b-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="2901b-139">Response</span></span>

<span data-ttu-id="2901b-140">В случае успешного выполнения этот метод `200 OK` возвращает код отклика и объект [воркбукворкшит](../resources/workbookworksheet.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="2901b-140">If successful, this method returns `200 OK` response code and [workbookWorksheet](../resources/workbookworksheet.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2901b-141">Пример</span><span class="sxs-lookup"><span data-stu-id="2901b-141">Example</span></span>
<span data-ttu-id="2901b-142">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="2901b-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2901b-143">Запрос</span><span class="sxs-lookup"><span data-stu-id="2901b-143">Request</span></span>
<span data-ttu-id="2901b-144">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="2901b-144">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="2901b-145">HTTP</span><span class="sxs-lookup"><span data-stu-id="2901b-145">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "worksheetcollection_add"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/add
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="2901b-146">C#</span><span class="sxs-lookup"><span data-stu-id="2901b-146">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/worksheetcollection-add-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="2901b-147">JavaScript</span><span class="sxs-lookup"><span data-stu-id="2901b-147">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/worksheetcollection-add-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="2901b-148">Цель — C</span><span class="sxs-lookup"><span data-stu-id="2901b-148">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/worksheetcollection-add-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="2901b-149">Отклик</span><span class="sxs-lookup"><span data-stu-id="2901b-149">Response</span></span>
<span data-ttu-id="2901b-p106">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="2901b-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookWorksheet"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 100

{
  "id": "id-value",
  "position": 99,
  "name": "name-value",
  "visibility": "visibility-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "WorksheetCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
