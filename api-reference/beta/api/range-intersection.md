---
title: 'Range: Intersection'
description: Возвращает объект диапазона, представляющий собой прямоугольное пересечение заданных диапазонов.
author: lumine2008
ms.openlocfilehash: 0ba9767c3c7d30ee5746b5a6723fd8103c1b8533
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344557"
---
# <a name="range-intersection"></a><span data-ttu-id="0816a-103">Range: Intersection</span><span class="sxs-lookup"><span data-stu-id="0816a-103">Range: Intersection</span></span>

> <span data-ttu-id="0816a-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="0816a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0816a-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0816a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0816a-106">Возвращает объект диапазона, представляющий собой прямоугольное пересечение заданных диапазонов.</span><span class="sxs-lookup"><span data-stu-id="0816a-106">Gets the range object that represents the rectangular intersection of the given ranges.</span></span>
## <a name="permissions"></a><span data-ttu-id="0816a-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="0816a-107">Permissions</span></span>
<span data-ttu-id="0816a-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0816a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0816a-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="0816a-110">Permission type</span></span>      | <span data-ttu-id="0816a-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="0816a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0816a-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="0816a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0816a-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0816a-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0816a-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="0816a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0816a-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0816a-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0816a-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="0816a-116">Application</span></span> | <span data-ttu-id="0816a-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0816a-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0816a-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="0816a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/Intersection
GET /workbook/worksheets/{id|name}/range(address='<address>')/Intersection
GET /workbook/tables/{id|name}/columns/{id|name}/range/Intersection

```
## <a name="request-headers"></a><span data-ttu-id="0816a-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="0816a-119">Request headers</span></span>
| <span data-ttu-id="0816a-120">Имя</span><span class="sxs-lookup"><span data-stu-id="0816a-120">Name</span></span>       | <span data-ttu-id="0816a-121">Описание</span><span class="sxs-lookup"><span data-stu-id="0816a-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0816a-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="0816a-122">Authorization</span></span>  | <span data-ttu-id="0816a-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="0816a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0816a-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0816a-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="0816a-p104">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="0816a-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0816a-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="0816a-128">Request body</span></span>
<span data-ttu-id="0816a-129">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="0816a-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="0816a-130">Параметр</span><span class="sxs-lookup"><span data-stu-id="0816a-130">Parameter</span></span>    | <span data-ttu-id="0816a-131">Тип</span><span class="sxs-lookup"><span data-stu-id="0816a-131">Type</span></span>   |<span data-ttu-id="0816a-132">Описание</span><span class="sxs-lookup"><span data-stu-id="0816a-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0816a-133">anotherRange</span><span class="sxs-lookup"><span data-stu-id="0816a-133">anotherRange</span></span>|<span data-ttu-id="0816a-134">string</span><span class="sxs-lookup"><span data-stu-id="0816a-134">string</span></span>|<span data-ttu-id="0816a-135">Объект или адрес диапазона, который будет использоваться для определения пересечения диапазонов.</span><span class="sxs-lookup"><span data-stu-id="0816a-135">The range object or range address that will be used to determine the intersection of ranges.</span></span>|

## <a name="response"></a><span data-ttu-id="0816a-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="0816a-136">Response</span></span>

<span data-ttu-id="0816a-137">В случае успеха этот метод возвращает код отклика `200 OK` и объект [Range](../resources/range.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="0816a-137">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0816a-138">Пример</span><span class="sxs-lookup"><span data-stu-id="0816a-138">Example</span></span>
<span data-ttu-id="0816a-139">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="0816a-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0816a-140">Запрос</span><span class="sxs-lookup"><span data-stu-id="0816a-140">Request</span></span>
<span data-ttu-id="0816a-141">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="0816a-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_intersection"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/Intersection
Content-type: application/json
Content-length: 42

{
  "anotherRange": "anotherRange-value"
}
```

##### <a name="response"></a><span data-ttu-id="0816a-142">Ответ</span><span class="sxs-lookup"><span data-stu-id="0816a-142">Response</span></span>
<span data-ttu-id="0816a-p105">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="0816a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: Intersection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->