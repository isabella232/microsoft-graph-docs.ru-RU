---
title: 'Воркбукворкшитпротектион: защита'
description: Защита листа. Выдает исключение, если лист защищен.
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: apiPageType
ms.openlocfilehash: 1ee9aff7f3f49da0c1b82ab4b953c4f3ae1a25e9
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48089891"
---
# <a name="workbookworksheetprotection-protect"></a><span data-ttu-id="4f884-104">Воркбукворкшитпротектион: защита</span><span class="sxs-lookup"><span data-stu-id="4f884-104">workbookWorksheetProtection: protect</span></span>

<span data-ttu-id="4f884-105">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="4f884-105">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="4f884-p102">Защита листа. Выдает исключение, если лист защищен.</span><span class="sxs-lookup"><span data-stu-id="4f884-p102">Protect a worksheet. It throws if the worksheet has been protected.</span></span>
## <a name="permissions"></a><span data-ttu-id="4f884-108">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4f884-108">Permissions</span></span>
<span data-ttu-id="4f884-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4f884-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4f884-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="4f884-111">Permission type</span></span>      | <span data-ttu-id="4f884-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="4f884-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4f884-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="4f884-113">Delegated (work or school account)</span></span> | <span data-ttu-id="4f884-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4f884-114">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4f884-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="4f884-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4f884-116">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4f884-116">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4f884-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="4f884-117">Application</span></span> | <span data-ttu-id="4f884-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4f884-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4f884-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="4f884-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/protect

```
## <a name="request-headers"></a><span data-ttu-id="4f884-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="4f884-120">Request headers</span></span>
| <span data-ttu-id="4f884-121">Имя</span><span class="sxs-lookup"><span data-stu-id="4f884-121">Name</span></span>       | <span data-ttu-id="4f884-122">Описание</span><span class="sxs-lookup"><span data-stu-id="4f884-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4f884-123">Авторизация</span><span class="sxs-lookup"><span data-stu-id="4f884-123">Authorization</span></span>  | <span data-ttu-id="4f884-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4f884-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4f884-126">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="4f884-126">Workbook-Session-Id</span></span>  | <span data-ttu-id="4f884-p105">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="4f884-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="4f884-129">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="4f884-129">Request body</span></span>
<span data-ttu-id="4f884-130">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="4f884-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4f884-131">Параметр</span><span class="sxs-lookup"><span data-stu-id="4f884-131">Parameter</span></span>    | <span data-ttu-id="4f884-132">Тип</span><span class="sxs-lookup"><span data-stu-id="4f884-132">Type</span></span>   |<span data-ttu-id="4f884-133">Описание</span><span class="sxs-lookup"><span data-stu-id="4f884-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4f884-134">options</span><span class="sxs-lookup"><span data-stu-id="4f884-134">options</span></span>|[<span data-ttu-id="4f884-135">воркбукворкшитпротектионоптионс</span><span class="sxs-lookup"><span data-stu-id="4f884-135">workbookWorksheetProtectionOptions</span></span>](../resources/workbookworksheetprotectionoptions.md)|<span data-ttu-id="4f884-p106">Необязательные параметры защиты листа.</span><span class="sxs-lookup"><span data-stu-id="4f884-p106">Optional. sheet protection options.</span></span>|

## <a name="response"></a><span data-ttu-id="4f884-138">Отклик</span><span class="sxs-lookup"><span data-stu-id="4f884-138">Response</span></span>

<span data-ttu-id="4f884-p107">В случае успешного выполнения этот метод возвращает код отклика `200 OK`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="4f884-p107">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4f884-141">Пример</span><span class="sxs-lookup"><span data-stu-id="4f884-141">Example</span></span>
<span data-ttu-id="4f884-142">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="4f884-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="4f884-143">Запрос</span><span class="sxs-lookup"><span data-stu-id="4f884-143">Request</span></span>
<span data-ttu-id="4f884-144">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="4f884-144">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="4f884-145">HTTP</span><span class="sxs-lookup"><span data-stu-id="4f884-145">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "workbookworksheetprotection_protect"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/protection/protect
Content-type: application/json
Content-length: 383

{
  "options": {
    "allowFormatCells": true,
    "allowFormatColumns": true,
    "allowFormatRows": true,
    "allowInsertColumns": true,
    "allowInsertRows": true,
    "allowInsertHyperlinks": true,
    "allowDeleteColumns": true,
    "allowDeleteRows": true,
    "allowSort": true,
    "allowAutoFilter": true,
    "allowPivotTables": true
  }
}
```
# <a name="c"></a>[<span data-ttu-id="4f884-146">C#</span><span class="sxs-lookup"><span data-stu-id="4f884-146">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/workbookworksheetprotection-protect-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="4f884-147">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4f884-147">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/workbookworksheetprotection-protect-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="4f884-148">Objective-C</span><span class="sxs-lookup"><span data-stu-id="4f884-148">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/workbookworksheetprotection-protect-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="4f884-149">Отклик</span><span class="sxs-lookup"><span data-stu-id="4f884-149">Response</span></span>
<span data-ttu-id="4f884-150">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="4f884-150">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "workbookWorksheetProtection: protect",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


