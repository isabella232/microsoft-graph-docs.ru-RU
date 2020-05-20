---
title: Получение конечной точки
description: Получение свойств и связей определенного объекта конечной точки.
localization_priority: Normal
doc_type: apiPageType
ms.prod: microsoft-identity-platform
author: davidmu1
ms.openlocfilehash: 61afceb23471306962ef5dbea895b0b5e5d38c48
ms.sourcegitcommit: 87966dcd42a0111c5c9987fcae0a491c92022938
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "44289859"
---
# <a name="get-endpoint"></a><span data-ttu-id="00bf6-103">Получение конечной точки</span><span class="sxs-lookup"><span data-stu-id="00bf6-103">Get endpoint</span></span>

<span data-ttu-id="00bf6-104">Получение свойств и связей определенного объекта [конечной точки](../resources/endpoint.md) .</span><span class="sxs-lookup"><span data-stu-id="00bf6-104">Retrieve the properties and relationships of a specific [endpoint](../resources/endpoint.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="00bf6-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="00bf6-105">Permissions</span></span>
<span data-ttu-id="00bf6-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="00bf6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="00bf6-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="00bf6-108">Permission type</span></span>      | <span data-ttu-id="00bf6-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="00bf6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="00bf6-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="00bf6-110">Delegated (work or school account)</span></span> | <span data-ttu-id="00bf6-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00bf6-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="00bf6-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="00bf6-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="00bf6-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="00bf6-113">Not supported.</span></span>    |
|<span data-ttu-id="00bf6-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="00bf6-114">Application</span></span> | <span data-ttu-id="00bf6-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00bf6-115">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="00bf6-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="00bf6-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/endpoints/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="00bf6-117">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="00bf6-117">Optional query parameters</span></span>
<span data-ttu-id="00bf6-118">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="00bf6-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="00bf6-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="00bf6-119">Request headers</span></span>
| <span data-ttu-id="00bf6-120">Имя</span><span class="sxs-lookup"><span data-stu-id="00bf6-120">Name</span></span>      |<span data-ttu-id="00bf6-121">Описание</span><span class="sxs-lookup"><span data-stu-id="00bf6-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="00bf6-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="00bf6-122">Authorization</span></span>  | <span data-ttu-id="00bf6-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="00bf6-p102">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="00bf6-125">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="00bf6-125">Request body</span></span>
<span data-ttu-id="00bf6-126">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="00bf6-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="00bf6-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="00bf6-127">Response</span></span>

<span data-ttu-id="00bf6-128">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и объект [конечной точки](../resources/endpoint.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="00bf6-128">If successful, this method returns a `200 OK` response code and an [Endpoint](../resources/endpoint.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="00bf6-129">Пример</span><span class="sxs-lookup"><span data-stu-id="00bf6-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="00bf6-130">Запрос</span><span class="sxs-lookup"><span data-stu-id="00bf6-130">Request</span></span>


# <a name="http"></a>[<span data-ttu-id="00bf6-131">HTTP</span><span class="sxs-lookup"><span data-stu-id="00bf6-131">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_endpoint"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/groups/{id}/endpoints/{id}
```

### <a name="response"></a><span data-ttu-id="00bf6-132">Отклик</span><span class="sxs-lookup"><span data-stu-id="00bf6-132">Response</span></span>
<span data-ttu-id="00bf6-133">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="00bf6-133">Here is an example of the response.</span></span>
><span data-ttu-id="00bf6-p103">Примечание. Представленный здесь объект отклика может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="00bf6-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.endpoint"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 208

{
  "capability": "Conversations",
  "providerId": "{Yammer GUID}",
  "providerName": "Yammer",
  "uri": "uri-value",
  "providerResourceId": "Yammer.FeedURL",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Get Endpoint",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
