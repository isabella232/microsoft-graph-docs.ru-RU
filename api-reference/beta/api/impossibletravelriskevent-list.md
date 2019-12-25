---
title: Список Импоссиблетравелрискевентс
description: Получение списка объектов импоссиблетравелрискевент.
localization_priority: Normal
doc_type: apiPageType
author: ''
ms.prod: ''
ms.openlocfilehash: 4b91ccb4af5d81a5c64fed916fff9663d99dc57a
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40869502"
---
# <a name="list-impossibletravelriskevents"></a><span data-ttu-id="d099a-103">Список Импоссиблетравелрискевентс</span><span class="sxs-lookup"><span data-stu-id="d099a-103">List impossibleTravelRiskEvents</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

>[!NOTE]
><span data-ttu-id="d099a-104">API **идентитирискевентс** устарел и не возвращает данные на 10 января 2020.</span><span class="sxs-lookup"><span data-stu-id="d099a-104">The **identityRiskEvents** API is deprecated and will stop returning data on January 10, 2020.</span></span> <span data-ttu-id="d099a-105">Дополнительные сведения см. [в разделе устаревшее API идентитирискевентс](https://developer.microsoft.com/office/blogs/deprecatation-of-the-identityriskevents-api/).</span><span class="sxs-lookup"><span data-stu-id="d099a-105">For details, see [Deprecation of the IdentityRiskEvents API](https://developer.microsoft.com/office/blogs/deprecatation-of-the-identityriskevents-api/).</span></span>

<span data-ttu-id="d099a-106">Получение списка объектов импоссиблетравелрискевент.</span><span class="sxs-lookup"><span data-stu-id="d099a-106">Retrieve a list of impossibletravelriskevent objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="d099a-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="d099a-107">Permissions</span></span>
<span data-ttu-id="d099a-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d099a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d099a-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="d099a-110">Permission type</span></span>      | <span data-ttu-id="d099a-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="d099a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d099a-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d099a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d099a-113">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="d099a-113">IdentityRiskEvent.Read.All</span></span>    |
|<span data-ttu-id="d099a-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="d099a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d099a-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d099a-115">Not supported.</span></span>    |
|<span data-ttu-id="d099a-116">Приложение</span><span class="sxs-lookup"><span data-stu-id="d099a-116">Application</span></span> | <span data-ttu-id="d099a-117">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="d099a-117">IdentityRiskEvent.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d099a-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="d099a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /impossibleTravelRiskEvents
```
## <a name="request-headers"></a><span data-ttu-id="d099a-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="d099a-119">Request headers</span></span>
| <span data-ttu-id="d099a-120">Имя</span><span class="sxs-lookup"><span data-stu-id="d099a-120">Name</span></span>      |<span data-ttu-id="d099a-121">Описание</span><span class="sxs-lookup"><span data-stu-id="d099a-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d099a-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="d099a-122">Authorization</span></span>  | <span data-ttu-id="d099a-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d099a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d099a-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d099a-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="d099a-p104">Идентификатор сеанса работы с книгой, определяющий, сохраняются ли изменения. Задавать не обязательно.</span><span class="sxs-lookup"><span data-stu-id="d099a-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d099a-128">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="d099a-128">Request body</span></span>
<span data-ttu-id="d099a-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="d099a-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d099a-130">Ответ</span><span class="sxs-lookup"><span data-stu-id="d099a-130">Response</span></span>

<span data-ttu-id="d099a-131">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и коллекцию объектов [импоссиблетравелрискевент](../resources/impossibletravelriskevent.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="d099a-131">If successful, this method returns a `200 OK` response code and collection of [impossibleTravelRiskEvent](../resources/impossibletravelriskevent.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d099a-132">Пример</span><span class="sxs-lookup"><span data-stu-id="d099a-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d099a-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="d099a-133">Request</span></span>
<span data-ttu-id="d099a-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="d099a-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_impossibletravelriskevents"
}-->
```http
GET https://graph.microsoft.com/v1.0/impossibleTravelRiskEvents
```
##### <a name="response"></a><span data-ttu-id="d099a-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="d099a-135">Response</span></span>
<span data-ttu-id="d099a-p105">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="d099a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.impossibleTravelRiskEvent",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 313

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.impossibleTravelRiskEvent",
      "closedDateTime": "2016-01-29T20:03:57.7872426Z",
      "createdDateTime": "2016-01-29T00:01:49.126468Z",
      "id": "22e65c1f-909a-42b5-c0d2-075f30e27887-0bfdc7a8-6a16-c33e-7de9-a60a28ae533b-15475553-dbc1-8879-5079-23b1edd25bab",
      "ipAddress": "176.10.104.240",
      "isAtypicalLocation": true,
      "location": "Bern, CH",
      "previousIPAddress": "95.31.18.119",
      "previousLocation": "Moskva, Russia, RU",
      "previousSigninDateTime": "2016-01-29T00:00:55.3859274Z",
      "riskEventDateTime": "2016-01-29T00:00:56.2255665Z",
      "riskEventStatus": "remediated",
      "riskLevel": "medium",
      "riskType": "ImpossibleTravelRiskEvent",
      "userAgent": "Mozilla",
      "userDisplayName": "Jon Doe",
      "userId": "0bfdc7a8-6a16-c33e-7de9-a60a28ae533b",
      "userPrincipalName": "jon@contoso.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "List impossibleTravelRiskEvents",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
