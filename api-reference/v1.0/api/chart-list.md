---
title: Список ChartCollection
description: Получение списка объектов диаграмм.
author: lumine2008
ms.openlocfilehash: 677e76deb00726c725f25ad7ac1ec9b5f0c77af3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2018
ms.locfileid: "27318167"
---
# <a name="list-chartcollection"></a><span data-ttu-id="f84cc-103">Список ChartCollection</span><span class="sxs-lookup"><span data-stu-id="f84cc-103">List ChartCollection</span></span>

<span data-ttu-id="f84cc-104">Получение списка объектов диаграмм.</span><span class="sxs-lookup"><span data-stu-id="f84cc-104">Retrieve a list of chart objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="f84cc-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="f84cc-105">Permissions</span></span>
<span data-ttu-id="f84cc-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f84cc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f84cc-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="f84cc-108">Permission type</span></span>      | <span data-ttu-id="f84cc-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="f84cc-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f84cc-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="f84cc-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f84cc-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f84cc-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f84cc-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="f84cc-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f84cc-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f84cc-113">Not supported.</span></span>    |
|<span data-ttu-id="f84cc-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="f84cc-114">Application</span></span> | <span data-ttu-id="f84cc-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f84cc-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f84cc-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="f84cc-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="f84cc-117">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="f84cc-117">Optional query parameters</span></span>
<span data-ttu-id="f84cc-118">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="f84cc-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f84cc-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="f84cc-119">Request headers</span></span>
| <span data-ttu-id="f84cc-120">Имя</span><span class="sxs-lookup"><span data-stu-id="f84cc-120">Name</span></span>      |<span data-ttu-id="f84cc-121">Описание</span><span class="sxs-lookup"><span data-stu-id="f84cc-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f84cc-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="f84cc-122">Authorization</span></span>  | <span data-ttu-id="f84cc-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="f84cc-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f84cc-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f84cc-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="f84cc-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="f84cc-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f84cc-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="f84cc-128">Request body</span></span>
<span data-ttu-id="f84cc-129">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="f84cc-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f84cc-130">Ответ</span><span class="sxs-lookup"><span data-stu-id="f84cc-130">Response</span></span>

<span data-ttu-id="f84cc-131">Успешно завершена, этот метод возвращает `200 OK` код ответа и коллекцию объектов [WorkbookChart](../resources/chart.md) в теле ответа.</span><span class="sxs-lookup"><span data-stu-id="f84cc-131">If successful, this method returns a `200 OK` response code and collection of [WorkbookChart](../resources/chart.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f84cc-132">Пример</span><span class="sxs-lookup"><span data-stu-id="f84cc-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f84cc-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="f84cc-133">Request</span></span>
<span data-ttu-id="f84cc-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="f84cc-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_chartcollection"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts
```
##### <a name="response"></a><span data-ttu-id="f84cc-135">Ответ</span><span class="sxs-lookup"><span data-stu-id="f84cc-135">Response</span></span>
<span data-ttu-id="f84cc-p104">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="f84cc-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChart",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 93

{
  "value": [
    {
      "id": "id-value",
      "height": 99,
      "left": 99
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List ChartCollection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->