---
title: 'ChartCollection: add'
description: Создает диаграмму.
author: lumine2008
ms.openlocfilehash: bfae5968c6a1131cb58bda80bd2587a68047bed9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332958"
---
# <a name="chartcollection-add"></a><span data-ttu-id="bba74-103">ChartCollection: add</span><span class="sxs-lookup"><span data-stu-id="bba74-103">ChartCollection: add</span></span>

<span data-ttu-id="bba74-104">Создает диаграмму.</span><span class="sxs-lookup"><span data-stu-id="bba74-104">Creates a new chart.</span></span>
## <a name="permissions"></a><span data-ttu-id="bba74-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="bba74-105">Permissions</span></span>
<span data-ttu-id="bba74-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bba74-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bba74-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="bba74-108">Permission type</span></span>      | <span data-ttu-id="bba74-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="bba74-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bba74-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="bba74-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bba74-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bba74-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="bba74-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="bba74-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bba74-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bba74-113">Not supported.</span></span>    |
|<span data-ttu-id="bba74-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="bba74-114">Application</span></span> | <span data-ttu-id="bba74-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bba74-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bba74-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="bba74-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/add

```
## <a name="request-headers"></a><span data-ttu-id="bba74-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="bba74-117">Request headers</span></span>
| <span data-ttu-id="bba74-118">Имя</span><span class="sxs-lookup"><span data-stu-id="bba74-118">Name</span></span>       | <span data-ttu-id="bba74-119">Описание</span><span class="sxs-lookup"><span data-stu-id="bba74-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="bba74-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="bba74-120">Authorization</span></span>  | <span data-ttu-id="bba74-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="bba74-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bba74-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="bba74-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="bba74-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="bba74-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="bba74-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="bba74-126">Request body</span></span>
<span data-ttu-id="bba74-127">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="bba74-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="bba74-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="bba74-128">Parameter</span></span>    | <span data-ttu-id="bba74-129">Тип</span><span class="sxs-lookup"><span data-stu-id="bba74-129">Type</span></span>   |<span data-ttu-id="bba74-130">Описание</span><span class="sxs-lookup"><span data-stu-id="bba74-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bba74-131">type</span><span class="sxs-lookup"><span data-stu-id="bba74-131">type</span></span>|<span data-ttu-id="bba74-132">строка</span><span class="sxs-lookup"><span data-stu-id="bba74-132">string</span></span>|<span data-ttu-id="bba74-133">Представляет тип диаграммы.</span><span class="sxs-lookup"><span data-stu-id="bba74-133">Represents the type of a chart.</span></span>  <span data-ttu-id="bba74-134">Возможные значения: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span><span class="sxs-lookup"><span data-stu-id="bba74-134">The possible values are: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span></span>|
|<span data-ttu-id="bba74-135">sourceData</span><span class="sxs-lookup"><span data-stu-id="bba74-135">sourceData</span></span>|<span data-ttu-id="bba74-136">Json</span><span class="sxs-lookup"><span data-stu-id="bba74-136">Json</span></span>|<span data-ttu-id="bba74-137">Объект Range, соответствующий исходным данным.</span><span class="sxs-lookup"><span data-stu-id="bba74-137">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="bba74-138">seriesBy</span><span class="sxs-lookup"><span data-stu-id="bba74-138">seriesBy</span></span>|<span data-ttu-id="bba74-139">string</span><span class="sxs-lookup"><span data-stu-id="bba74-139">string</span></span>|<span data-ttu-id="bba74-140">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="bba74-140">Optional.</span></span> <span data-ttu-id="bba74-141">Указывает, что способ столбцы или строки используются в качестве рядов данных на диаграмме.</span><span class="sxs-lookup"><span data-stu-id="bba74-141">Specifies the way columns or rows are used as data series on the chart.</span></span>  <span data-ttu-id="bba74-142">Возможные значения: `Auto`, `Columns`, `Rows`.</span><span class="sxs-lookup"><span data-stu-id="bba74-142">The possible values are: `Auto`, `Columns`, `Rows`.</span></span>|

## <a name="response"></a><span data-ttu-id="bba74-143">Ответ</span><span class="sxs-lookup"><span data-stu-id="bba74-143">Response</span></span>

<span data-ttu-id="bba74-144">Успешно завершена, этот метод возвращает `200 OK` код ответа и объект [WorkbookChart](../resources/chart.md) в теле ответа.</span><span class="sxs-lookup"><span data-stu-id="bba74-144">If successful, this method returns `200 OK` response code and [WorkbookChart](../resources/chart.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bba74-145">Пример</span><span class="sxs-lookup"><span data-stu-id="bba74-145">Example</span></span>
<span data-ttu-id="bba74-146">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="bba74-146">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="bba74-147">Запрос</span><span class="sxs-lookup"><span data-stu-id="bba74-147">Request</span></span>
<span data-ttu-id="bba74-148">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="bba74-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/add
Content-type: application/json
Content-length: 94

{
  "type": "ColumnStacked",
  "sourceData": "A1:B1",
  "seriesBy": "Auto"
}
```

##### <a name="response"></a><span data-ttu-id="bba74-149">Ответ</span><span class="sxs-lookup"><span data-stu-id="bba74-149">Response</span></span>
<span data-ttu-id="bba74-p106">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="bba74-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
<!-- {
  "type": "#page.annotation",
  "description": "ChartCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
