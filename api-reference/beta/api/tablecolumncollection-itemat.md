---
title: 'TableColumnCollection: ItemAt'
description: Возвращает столбец на основании его позиции в коллекции.
author: lumine2008
ms.openlocfilehash: bcb72a511bfed9adcc0219a5b85402b1931a795d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314065"
---
# <a name="tablecolumncollection-itemat"></a><span data-ttu-id="9d875-103">TableColumnCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="9d875-103">TableColumnCollection: ItemAt</span></span>

> <span data-ttu-id="9d875-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="9d875-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9d875-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9d875-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9d875-106">Возвращает столбец на основании его позиции в коллекции.</span><span class="sxs-lookup"><span data-stu-id="9d875-106">Gets a column based on its position in the collection.</span></span>
## <a name="permissions"></a><span data-ttu-id="9d875-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="9d875-107">Permissions</span></span>
<span data-ttu-id="9d875-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9d875-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9d875-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="9d875-110">Permission type</span></span>      | <span data-ttu-id="9d875-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="9d875-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9d875-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="9d875-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9d875-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9d875-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9d875-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="9d875-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9d875-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9d875-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9d875-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="9d875-116">Application</span></span> | <span data-ttu-id="9d875-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9d875-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9d875-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="9d875-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/ItemAt
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="9d875-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="9d875-119">Request headers</span></span>
| <span data-ttu-id="9d875-120">Имя</span><span class="sxs-lookup"><span data-stu-id="9d875-120">Name</span></span>       | <span data-ttu-id="9d875-121">Описание</span><span class="sxs-lookup"><span data-stu-id="9d875-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9d875-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="9d875-122">Authorization</span></span>  | <span data-ttu-id="9d875-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="9d875-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9d875-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="9d875-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="9d875-p104">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="9d875-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="9d875-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="9d875-128">Request body</span></span>
<span data-ttu-id="9d875-129">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="9d875-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9d875-130">Параметр</span><span class="sxs-lookup"><span data-stu-id="9d875-130">Parameter</span></span>    | <span data-ttu-id="9d875-131">Тип</span><span class="sxs-lookup"><span data-stu-id="9d875-131">Type</span></span>   |<span data-ttu-id="9d875-132">Описание</span><span class="sxs-lookup"><span data-stu-id="9d875-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9d875-133">index</span><span class="sxs-lookup"><span data-stu-id="9d875-133">index</span></span>|<span data-ttu-id="9d875-134">number</span><span class="sxs-lookup"><span data-stu-id="9d875-134">number</span></span>|<span data-ttu-id="9d875-p105">Значение индекса получаемого объекта. Используется нулевой индекс.</span><span class="sxs-lookup"><span data-stu-id="9d875-p105">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="9d875-137">Отклик</span><span class="sxs-lookup"><span data-stu-id="9d875-137">Response</span></span>

<span data-ttu-id="9d875-138">В случае успеха этот метод возвращает код отклика `200 OK` и объект [TableColumn](../resources/tablecolumn.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="9d875-138">If successful, this method returns `200 OK` response code and [TableColumn](../resources/tablecolumn.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9d875-139">Пример</span><span class="sxs-lookup"><span data-stu-id="9d875-139">Example</span></span>
<span data-ttu-id="9d875-140">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="9d875-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9d875-141">Запрос</span><span class="sxs-lookup"><span data-stu-id="9d875-141">Request</span></span>
<span data-ttu-id="9d875-142">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="9d875-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablecolumncollection_itemat"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/columns/ItemAt
Content-type: application/json
Content-length: 20

{
  "index": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="9d875-143">Ответ</span><span class="sxs-lookup"><span data-stu-id="9d875-143">Response</span></span>
<span data-ttu-id="9d875-p106">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="9d875-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableColumn"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 81

{
  "id": 99,
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableColumnCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->