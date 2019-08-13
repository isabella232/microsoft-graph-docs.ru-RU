---
title: 'RangeFormat: autofitRows'
description: Изменяет высоту строк текущего диапазона так, чтобы она была оптимальной, с учетом текущих данных в столбцах.
localization_priority: Normal
author: lumine2008
ms.prod: excel
doc_type: apiPageType
ms.openlocfilehash: 0a7c813928d14f1d8cb3d4ed9405de3513b289c4
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "36368949"
---
# <a name="rangeformat-autofitrows"></a><span data-ttu-id="ef676-103">RangeFormat: autofitRows</span><span class="sxs-lookup"><span data-stu-id="ef676-103">RangeFormat: autofitRows</span></span>

<span data-ttu-id="ef676-104">Изменяет высоту строк текущего диапазона так, чтобы она была оптимальной, с учетом текущих данных в столбцах.</span><span class="sxs-lookup"><span data-stu-id="ef676-104">Changes the height of the rows of the current range to achieve the best fit, based on the current data in the columns.</span></span>
## <a name="permissions"></a><span data-ttu-id="ef676-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="ef676-105">Permissions</span></span>
<span data-ttu-id="ef676-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ef676-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ef676-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="ef676-108">Permission type</span></span>      | <span data-ttu-id="ef676-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="ef676-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ef676-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="ef676-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ef676-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ef676-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ef676-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="ef676-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ef676-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ef676-113">Not supported.</span></span>    |
|<span data-ttu-id="ef676-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="ef676-114">Application</span></span> | <span data-ttu-id="ef676-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ef676-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ef676-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="ef676-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/format/autofitRows
POST /workbook/worksheets/{id|name}/range(address='<address>')/format/autofitRows
POST /workbook/tables/{id|name}/columns/{id|name}/range/format/autofitRows

```
## <a name="request-headers"></a><span data-ttu-id="ef676-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="ef676-117">Request headers</span></span>
| <span data-ttu-id="ef676-118">Имя</span><span class="sxs-lookup"><span data-stu-id="ef676-118">Name</span></span>       | <span data-ttu-id="ef676-119">Описание</span><span class="sxs-lookup"><span data-stu-id="ef676-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ef676-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="ef676-120">Authorization</span></span>  | <span data-ttu-id="ef676-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ef676-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ef676-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="ef676-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="ef676-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="ef676-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ef676-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="ef676-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="ef676-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="ef676-127">Response</span></span>

<span data-ttu-id="ef676-p104">В случае успешного выполнения этот метод возвращает код отклика `200 OK`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="ef676-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ef676-130">Пример</span><span class="sxs-lookup"><span data-stu-id="ef676-130">Example</span></span>
<span data-ttu-id="ef676-131">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="ef676-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="ef676-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="ef676-132">Request</span></span>
<span data-ttu-id="ef676-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="ef676-133">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="ef676-134">HTTP</span><span class="sxs-lookup"><span data-stu-id="ef676-134">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "rangeformat_autofitrows"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format/autofitRows
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="ef676-135">C#</span><span class="sxs-lookup"><span data-stu-id="ef676-135">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/rangeformat-autofitrows-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="ef676-136">JavaScript</span><span class="sxs-lookup"><span data-stu-id="ef676-136">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/rangeformat-autofitrows-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="ef676-137">Цель — C</span><span class="sxs-lookup"><span data-stu-id="ef676-137">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/rangeformat-autofitrows-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="ef676-138">Java</span><span class="sxs-lookup"><span data-stu-id="ef676-138">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/rangeformat-autofitrows-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="ef676-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="ef676-139">Response</span></span>
<span data-ttu-id="ef676-140">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="ef676-140">Here is an example of the response.</span></span> 
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
  "description": "RangeFormat: autofitRows",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
