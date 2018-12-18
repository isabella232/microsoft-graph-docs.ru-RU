---
title: 'Range: LastCell'
description: .
author: lumine2008
ms.openlocfilehash: 90087ab5e5000b096092e664abe19b7e384e310b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310124"
---
# <a name="range-lastcell"></a><span data-ttu-id="38e5f-103">Range: LastCell</span><span class="sxs-lookup"><span data-stu-id="38e5f-103">Range: LastCell</span></span>

> <span data-ttu-id="38e5f-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="38e5f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="38e5f-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="38e5f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="38e5f-p102">Возвращает последнюю ячейку в диапазоне. Например, последняя ячейка диапазона B2:D5 — D5.</span><span class="sxs-lookup"><span data-stu-id="38e5f-p102">Gets the last cell within the range. For example, the last cell of "B2:D5" is "D5".</span></span>
## <a name="permissions"></a><span data-ttu-id="38e5f-108">Разрешения</span><span class="sxs-lookup"><span data-stu-id="38e5f-108">Permissions</span></span>
<span data-ttu-id="38e5f-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38e5f-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="38e5f-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="38e5f-111">Permission type</span></span>      | <span data-ttu-id="38e5f-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="38e5f-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="38e5f-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="38e5f-113">Delegated (work or school account)</span></span> | <span data-ttu-id="38e5f-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="38e5f-114">Files.ReadWrite</span></span>    |
|<span data-ttu-id="38e5f-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="38e5f-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="38e5f-116">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="38e5f-116">Files.ReadWrite</span></span>    |
|<span data-ttu-id="38e5f-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="38e5f-117">Application</span></span> | <span data-ttu-id="38e5f-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="38e5f-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="38e5f-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="38e5f-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/LastCell
GET /workbook/worksheets/{id|name}/range(address='<address>')/LastCell
GET /workbook/tables/{id|name}/columns/{id|name}/range/LastCell

```
## <a name="request-headers"></a><span data-ttu-id="38e5f-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="38e5f-120">Request headers</span></span>
| <span data-ttu-id="38e5f-121">Имя</span><span class="sxs-lookup"><span data-stu-id="38e5f-121">Name</span></span>       | <span data-ttu-id="38e5f-122">Описание</span><span class="sxs-lookup"><span data-stu-id="38e5f-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="38e5f-123">Авторизация</span><span class="sxs-lookup"><span data-stu-id="38e5f-123">Authorization</span></span>  | <span data-ttu-id="38e5f-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="38e5f-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="38e5f-126">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="38e5f-126">Workbook-Session-Id</span></span>  | <span data-ttu-id="38e5f-p105">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="38e5f-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="38e5f-129">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="38e5f-129">Request body</span></span>

## <a name="response"></a><span data-ttu-id="38e5f-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="38e5f-130">Response</span></span>

<span data-ttu-id="38e5f-131">В случае успеха этот метод возвращает код отклика `200 OK` и объект [Range](../resources/range.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="38e5f-131">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="38e5f-132">Пример</span><span class="sxs-lookup"><span data-stu-id="38e5f-132">Example</span></span>
<span data-ttu-id="38e5f-133">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="38e5f-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="38e5f-134">Запрос</span><span class="sxs-lookup"><span data-stu-id="38e5f-134">Request</span></span>
<span data-ttu-id="38e5f-135">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="38e5f-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_lastcell"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/LastCell
```

##### <a name="response"></a><span data-ttu-id="38e5f-136">Ответ</span><span class="sxs-lookup"><span data-stu-id="38e5f-136">Response</span></span>
<span data-ttu-id="38e5f-p106">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="38e5f-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: LastCell",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->