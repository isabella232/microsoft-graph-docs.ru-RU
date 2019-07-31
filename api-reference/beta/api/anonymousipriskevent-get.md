---
title: Получение объекта anonymousIpRiskEvent
description: Получение свойств и связей объекта анонимаусиприскевент.
localization_priority: Normal
doc_type: apiPageType
ms.prod: ''
author: ''
ms.openlocfilehash: dd89350360f045659697da747525bf0bfa6ec96a
ms.sourcegitcommit: 2c62457e57467b8d50f21b255b553106a9a5d8d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2019
ms.locfileid: "35945587"
---
# <a name="get-anonymousipriskevent"></a><span data-ttu-id="8f866-103">Получение объекта anonymousIpRiskEvent</span><span class="sxs-lookup"><span data-stu-id="8f866-103">Get anonymousIpRiskEvent</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="8f866-104">Получение свойств и связей объекта анонимаусиприскевент.</span><span class="sxs-lookup"><span data-stu-id="8f866-104">Retrieve the properties and relationships of an anonymousipriskevent object.</span></span>
## <a name="permissions"></a><span data-ttu-id="8f866-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="8f866-105">Permissions</span></span>
<span data-ttu-id="8f866-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8f866-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8f866-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="8f866-108">Permission type</span></span>      | <span data-ttu-id="8f866-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="8f866-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8f866-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8f866-110">Delegated (work or school account)</span></span> | <span data-ttu-id="8f866-111">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="8f866-111">IdentityRiskEvent.Read.All</span></span>    |
|<span data-ttu-id="8f866-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="8f866-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8f866-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f866-113">Not supported.</span></span>    |
|<span data-ttu-id="8f866-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="8f866-114">Application</span></span> | <span data-ttu-id="8f866-115">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="8f866-115">IdentityRiskEvent.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8f866-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="8f866-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /anonymousIpRiskEvents/{id}
```

## <a name="request-headers"></a><span data-ttu-id="8f866-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="8f866-117">Request headers</span></span>
| <span data-ttu-id="8f866-118">Имя</span><span class="sxs-lookup"><span data-stu-id="8f866-118">Name</span></span>      |<span data-ttu-id="8f866-119">Описание</span><span class="sxs-lookup"><span data-stu-id="8f866-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="8f866-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="8f866-120">Authorization</span></span>  | <span data-ttu-id="8f866-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="8f866-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8f866-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="8f866-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="8f866-p103">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="8f866-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="8f866-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="8f866-126">Request body</span></span>
<span data-ttu-id="8f866-127">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="8f866-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8f866-128">Ответ</span><span class="sxs-lookup"><span data-stu-id="8f866-128">Response</span></span>

<span data-ttu-id="8f866-129">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и объект [анонимаусиприскевент](../resources/anonymousipriskevent.md) в значении тела отклика.</span><span class="sxs-lookup"><span data-stu-id="8f866-129">If successful, this method returns a `200 OK` response code and [anonymousIpRiskEvent](../resources/anonymousipriskevent.md) object in the value of response body.</span></span>
## <a name="example"></a><span data-ttu-id="8f866-130">Пример</span><span class="sxs-lookup"><span data-stu-id="8f866-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8f866-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="8f866-131">Request</span></span>
<span data-ttu-id="8f866-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="8f866-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_anonymousipriskevent"
}-->
```http
GET https://graph.microsoft.com/v1.0/anonymousIpRiskEvents/2016-01-29T00:00:56.22556656a56d0b2-3c51-7c5e-bc1a-1ccdb3bd9c71
```
##### <a name="response"></a><span data-ttu-id="8f866-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="8f866-133">Response</span></span>
<span data-ttu-id="8f866-p104">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="8f866-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.anonymousIpRiskEvent"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 237

{
  "closedDateTime": "2016-01-29T20:03:57.7872426Z",
  "createdDateTime": "2016-01-29T00:01:49.126468Z",
  "id": "2016-01-29T00:00:56.22556656a56d0b2-3c51-7c5e-bc1a-1ccdb3bd9c71",
  "ipAddress": null,
  "location": null,
  "riskEventDateTime": "2016-01-29T00:00:56.2255665Z",
  "riskEventStatus": "remediated",
  "riskLevel": "medium",
  "riskType": "AnonymousIpRiskEvent",
  "userDisplayName": "Jon Doe",
  "userId": "6a56d0b2-3c51-7c5e-bc1a-1ccdb3bd9c71",
  "userPrincipalName": "jon@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Get anonymousIpRiskEvent",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
