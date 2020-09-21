---
title: 'Воркбукчартколлектион: Итемат'
description: Получает объект воркбукчарт, основанный на его позиции в коллекции.
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: apiPageType
ms.openlocfilehash: bb3dfa39d16859068307dde8c744e40b7ab5ad81
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47983067"
---
# <a name="chartcollection-itemat"></a><span data-ttu-id="c0e61-103">ChartCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="c0e61-103">ChartCollection: ItemAt</span></span>

<span data-ttu-id="c0e61-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="c0e61-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="c0e61-105">Возвращает диаграмму на основании сведений о ее позиции в коллекции.</span><span class="sxs-lookup"><span data-stu-id="c0e61-105">Gets a chart based on its position in the collection.</span></span>
## <a name="permissions"></a><span data-ttu-id="c0e61-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="c0e61-106">Permissions</span></span>
<span data-ttu-id="c0e61-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c0e61-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c0e61-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="c0e61-109">Permission type</span></span>      | <span data-ttu-id="c0e61-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="c0e61-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c0e61-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c0e61-111">Delegated (work or school account)</span></span> | <span data-ttu-id="c0e61-112">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c0e61-112">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c0e61-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="c0e61-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c0e61-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c0e61-114">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c0e61-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="c0e61-115">Application</span></span> | <span data-ttu-id="c0e61-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c0e61-116">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c0e61-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="c0e61-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="c0e61-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="c0e61-118">Request headers</span></span>
| <span data-ttu-id="c0e61-119">Имя</span><span class="sxs-lookup"><span data-stu-id="c0e61-119">Name</span></span>       | <span data-ttu-id="c0e61-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c0e61-120">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c0e61-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="c0e61-121">Authorization</span></span>  | <span data-ttu-id="c0e61-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="c0e61-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c0e61-124">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c0e61-124">Workbook-Session-Id</span></span>  | <span data-ttu-id="c0e61-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="c0e61-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c0e61-127">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="c0e61-127">Request body</span></span>
<span data-ttu-id="c0e61-128">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="c0e61-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c0e61-129">Параметр</span><span class="sxs-lookup"><span data-stu-id="c0e61-129">Parameter</span></span>    | <span data-ttu-id="c0e61-130">Тип</span><span class="sxs-lookup"><span data-stu-id="c0e61-130">Type</span></span>   |<span data-ttu-id="c0e61-131">Описание</span><span class="sxs-lookup"><span data-stu-id="c0e61-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c0e61-132">index</span><span class="sxs-lookup"><span data-stu-id="c0e61-132">index</span></span>|<span data-ttu-id="c0e61-133">number</span><span class="sxs-lookup"><span data-stu-id="c0e61-133">number</span></span>|<span data-ttu-id="c0e61-p104">Значение индекса получаемого объекта. Используется нулевой индекс.</span><span class="sxs-lookup"><span data-stu-id="c0e61-p104">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="c0e61-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="c0e61-136">Response</span></span>

<span data-ttu-id="c0e61-137">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и объект [воркбукчарт](../resources/workbookchart.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="c0e61-137">If successful, this method returns `200 OK` response code and [workbookChart](../resources/workbookchart.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c0e61-138">Пример</span><span class="sxs-lookup"><span data-stu-id="c0e61-138">Example</span></span>
<span data-ttu-id="c0e61-139">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="c0e61-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c0e61-140">Запрос</span><span class="sxs-lookup"><span data-stu-id="c0e61-140">Request</span></span>
<span data-ttu-id="c0e61-141">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="c0e61-141">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="c0e61-142">HTTP</span><span class="sxs-lookup"><span data-stu-id="c0e61-142">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "chartcollection_itemat"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/ItemAt
Content-type: application/json
Content-length: 20

{
  "index": 8
}
```
# <a name="javascript"></a>[<span data-ttu-id="c0e61-143">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c0e61-143">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/chartcollection-itemat-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="c0e61-144">Objective-C</span><span class="sxs-lookup"><span data-stu-id="c0e61-144">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/chartcollection-itemat-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="c0e61-145">Отклик</span><span class="sxs-lookup"><span data-stu-id="c0e61-145">Response</span></span>
<span data-ttu-id="c0e61-p105">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="c0e61-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChart"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "height": 99,
  "left": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "ChartCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


