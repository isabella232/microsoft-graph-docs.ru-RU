---
title: 'Range: merge'
description: Объединяет ячейки диапазона в одну область на листе.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 264cde927a2525e6a0e7bdc672da153c96f3e490
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823214"
---
# <a name="range-merge"></a><span data-ttu-id="11107-103">Range: merge</span><span class="sxs-lookup"><span data-stu-id="11107-103">Range: merge</span></span>

<span data-ttu-id="11107-104">Объединяет ячейки диапазона в одну область на листе.</span><span class="sxs-lookup"><span data-stu-id="11107-104">Merge the range cells into one region in the worksheet.</span></span>
## <a name="permissions"></a><span data-ttu-id="11107-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="11107-105">Permissions</span></span>
<span data-ttu-id="11107-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="11107-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="11107-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="11107-108">Permission type</span></span>      | <span data-ttu-id="11107-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="11107-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="11107-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="11107-110">Delegated (work or school account)</span></span> | <span data-ttu-id="11107-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="11107-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="11107-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="11107-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="11107-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="11107-113">Not supported.</span></span>    |
|<span data-ttu-id="11107-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="11107-114">Application</span></span> | <span data-ttu-id="11107-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="11107-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="11107-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="11107-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/merge
POST /workbook/worksheets/{id|name}/range(address='<address>')/merge
POST /workbook/tables/{id|name}/columns/{id|name}/range/merge

```
## <a name="request-headers"></a><span data-ttu-id="11107-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="11107-117">Request headers</span></span>
| <span data-ttu-id="11107-118">Имя</span><span class="sxs-lookup"><span data-stu-id="11107-118">Name</span></span>       | <span data-ttu-id="11107-119">Описание</span><span class="sxs-lookup"><span data-stu-id="11107-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="11107-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="11107-120">Authorization</span></span>  | <span data-ttu-id="11107-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="11107-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="11107-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="11107-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="11107-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="11107-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="11107-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="11107-126">Request body</span></span>
<span data-ttu-id="11107-127">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="11107-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="11107-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="11107-128">Parameter</span></span>    | <span data-ttu-id="11107-129">Тип</span><span class="sxs-lookup"><span data-stu-id="11107-129">Type</span></span>   |<span data-ttu-id="11107-130">Описание</span><span class="sxs-lookup"><span data-stu-id="11107-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="11107-131">across</span><span class="sxs-lookup"><span data-stu-id="11107-131">across</span></span>|<span data-ttu-id="11107-132">boolean</span><span class="sxs-lookup"><span data-stu-id="11107-132">boolean</span></span>|<span data-ttu-id="11107-p104">Необязательный параметр. Установите значение true, чтобы объединить ячейки в каждой строке заданного диапазона как отдельные объединенные ячейки. Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="11107-p104">Optional. Set true to merge cells in each row of the specified range as separate merged cells. The default value is false.</span></span>|

## <a name="response"></a><span data-ttu-id="11107-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="11107-136">Response</span></span>

<span data-ttu-id="11107-p105">В случае успешного выполнения этот метод возвращает код отклика `200 OK`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="11107-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="11107-139">Пример</span><span class="sxs-lookup"><span data-stu-id="11107-139">Example</span></span>
<span data-ttu-id="11107-140">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="11107-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="11107-141">Запрос</span><span class="sxs-lookup"><span data-stu-id="11107-141">Request</span></span>
<span data-ttu-id="11107-142">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="11107-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_merge"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/merge
Content-type: application/json
Content-length: 20

{
  "across": true
}
```

##### <a name="response"></a><span data-ttu-id="11107-143">Ответ</span><span class="sxs-lookup"><span data-stu-id="11107-143">Response</span></span>
<span data-ttu-id="11107-144">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="11107-144">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: merge",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
