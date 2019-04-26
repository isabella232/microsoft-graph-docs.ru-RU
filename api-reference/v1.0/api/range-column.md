---
title: 'Range: Column'
description: Возвращает столбец в диапазоне.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 21338edb35c8e3e7c060d0f4a03e7e3e77f4e60b
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32575270"
---
# <a name="range-column"></a><span data-ttu-id="6adb3-103">Range: Column</span><span class="sxs-lookup"><span data-stu-id="6adb3-103">Range: Column</span></span>

<span data-ttu-id="6adb3-104">Возвращает столбец в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="6adb3-104">Gets a column contained in the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="6adb3-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="6adb3-105">Permissions</span></span>
<span data-ttu-id="6adb3-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6adb3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6adb3-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="6adb3-108">Permission type</span></span>      | <span data-ttu-id="6adb3-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="6adb3-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6adb3-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6adb3-110">Delegated (work or school account)</span></span> | <span data-ttu-id="6adb3-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6adb3-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6adb3-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="6adb3-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6adb3-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6adb3-113">Not supported.</span></span>    |
|<span data-ttu-id="6adb3-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="6adb3-114">Application</span></span> | <span data-ttu-id="6adb3-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6adb3-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6adb3-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="6adb3-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/column
GET /workbook/worksheets/{id|name}/range(address='<address>')/column
GET /workbook/tables/{id|name}/columns/{id|name}/range/column

```
## <a name="request-headers"></a><span data-ttu-id="6adb3-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="6adb3-117">Request headers</span></span>
| <span data-ttu-id="6adb3-118">Имя</span><span class="sxs-lookup"><span data-stu-id="6adb3-118">Name</span></span>       | <span data-ttu-id="6adb3-119">Описание</span><span class="sxs-lookup"><span data-stu-id="6adb3-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6adb3-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="6adb3-120">Authorization</span></span>  | <span data-ttu-id="6adb3-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6adb3-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6adb3-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6adb3-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="6adb3-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="6adb3-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="path-parameters"></a><span data-ttu-id="6adb3-126">Параметры пути</span><span class="sxs-lookup"><span data-stu-id="6adb3-126">Path parameters</span></span>
<span data-ttu-id="6adb3-127">В пути запроса укажите следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="6adb3-127">In the request path, provide the following parameters.</span></span>

| <span data-ttu-id="6adb3-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="6adb3-128">Parameter</span></span>    | <span data-ttu-id="6adb3-129">Тип</span><span class="sxs-lookup"><span data-stu-id="6adb3-129">Type</span></span>   |<span data-ttu-id="6adb3-130">Описание</span><span class="sxs-lookup"><span data-stu-id="6adb3-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6adb3-131">column</span><span class="sxs-lookup"><span data-stu-id="6adb3-131">column</span></span>|<span data-ttu-id="6adb3-132">Int32</span><span class="sxs-lookup"><span data-stu-id="6adb3-132">Int32</span></span>|<span data-ttu-id="6adb3-p104">Номер столбца диапазона, который требуется извлечь. Используется нулевой индекс.</span><span class="sxs-lookup"><span data-stu-id="6adb3-p104">Column number of the range to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="6adb3-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="6adb3-135">Response</span></span>

<span data-ttu-id="6adb3-136">В случае успеха этот метод возвращает код отклика `200 OK` и объект [Range](../resources/range.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="6adb3-136">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6adb3-137">Пример</span><span class="sxs-lookup"><span data-stu-id="6adb3-137">Example</span></span>
<span data-ttu-id="6adb3-138">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="6adb3-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="6adb3-139">Запрос</span><span class="sxs-lookup"><span data-stu-id="6adb3-139">Request</span></span>
<span data-ttu-id="6adb3-140">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="6adb3-140">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_column"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/column(column=5)
```

##### <a name="response"></a><span data-ttu-id="6adb3-141">Отклик</span><span class="sxs-lookup"><span data-stu-id="6adb3-141">Response</span></span>
<span data-ttu-id="6adb3-p105">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="6adb3-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
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
  "description": "Range: Column",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
