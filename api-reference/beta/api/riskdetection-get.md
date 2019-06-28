---
title: Получение Рискдетектион
description: Получение свойств объекта **рискдетектион** .
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 5d6484d06505f03950aaf5de7247c6e26b359754
ms.sourcegitcommit: e0de4e41773e361752870411d1b1a74270738127
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/28/2019
ms.locfileid: "35349448"
---
# <a name="get-riskdetection"></a><span data-ttu-id="a65b2-103">Получение Рискдетектион</span><span class="sxs-lookup"><span data-stu-id="a65b2-103">Get riskDetection</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="a65b2-104">Получение свойств объекта **рискдетектион** .</span><span class="sxs-lookup"><span data-stu-id="a65b2-104">Retrieve the properties of a **riskDetection** object.</span></span>

>[!NOTE]
><span data-ttu-id="a65b2-105">Для использования API обнаружения рисков необходима лицензия Azure AD Premium P2.</span><span class="sxs-lookup"><span data-stu-id="a65b2-105">You must have an Azure AD Premium P2 license to use the risk detection API.</span></span>

## <a name="permissions"></a><span data-ttu-id="a65b2-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="a65b2-106">Permissions</span></span>
<span data-ttu-id="a65b2-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a65b2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a65b2-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="a65b2-109">Permission type</span></span>      | <span data-ttu-id="a65b2-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="a65b2-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a65b2-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a65b2-111">Delegated (work or school account)</span></span> | <span data-ttu-id="a65b2-112">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="a65b2-112">IdentityRiskEvent.Read.All</span></span>    |
|<span data-ttu-id="a65b2-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="a65b2-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a65b2-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a65b2-114">Not supported.</span></span>    |
|<span data-ttu-id="a65b2-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="a65b2-115">Application</span></span> | <span data-ttu-id="a65b2-116">IdentityRiskEvent.Read.All</span><span class="sxs-lookup"><span data-stu-id="a65b2-116">IdentityRiskEvent.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a65b2-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="a65b2-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /riskDetections/{id}
```

## <a name="request-headers"></a><span data-ttu-id="a65b2-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="a65b2-118">Request headers</span></span>
| <span data-ttu-id="a65b2-119">Имя</span><span class="sxs-lookup"><span data-stu-id="a65b2-119">Name</span></span>      |<span data-ttu-id="a65b2-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a65b2-120">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a65b2-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="a65b2-121">Authorization</span></span>  | <span data-ttu-id="a65b2-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a65b2-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a65b2-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a65b2-124">Content-Type</span></span> | <span data-ttu-id="a65b2-125">application/json</span><span class="sxs-lookup"><span data-stu-id="a65b2-125">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="a65b2-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="a65b2-126">Request body</span></span>
<span data-ttu-id="a65b2-127">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="a65b2-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a65b2-128">Ответ</span><span class="sxs-lookup"><span data-stu-id="a65b2-128">Response</span></span>

<span data-ttu-id="a65b2-129">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и объект [рискдетектион](../resources/riskDetection.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="a65b2-129">If successful, this method returns a `200 OK` response code and a [riskDetection](../resources/riskDetection.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a65b2-130">Пример</span><span class="sxs-lookup"><span data-stu-id="a65b2-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a65b2-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="a65b2-131">Request</span></span>
<span data-ttu-id="a65b2-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="a65b2-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_riskDetection",
  "sampleKeys": ["c2b6c2b9-dddc-acd0-2b39-d519d803dbc3"]
}-->
```http
GET https://graph.microsoft.com/beta/riskDetections/c2b6c2b9-dddc-acd0-2b39-d519d803dbc3
```
##### <a name="response"></a><span data-ttu-id="a65b2-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="a65b2-133">Response</span></span>
<span data-ttu-id="a65b2-134">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="a65b2-134">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.riskDetection"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "6a5874ca-abcd-9d82-5ad39bd71600",
    "requestId": "6a5874ca-abcd-9d82-5ad39bd71600",
    "correlationId": "abcd74ca-9823-4b1c-9d82-5ad39bd71600",
    "riskType": "unfamiliarFeatures",
    "riskState": "remediated",
    "riskLevel": "medium",
    "riskDetail": "userPerformedSecuredPasswordReset",
    "source": "activeDirectory",
    "detectionTimingType": "realtime",
    "activity": "signin",
    "tokenIssuerType": "Azure Active Directory",
    "ipAddress": "123.456.7.89",
    "location": {
        "city": "Seattle",
        "state": "Washington",
        "countryOrRegion": "US",
        "geoCoordinates": null
    },
    "activityDateTime": "2018-09-05T00:09:18.7822851Z",
    "detectedDateTime": "2018-09-05T00:11:27.773602Z",
    "lastUpdatedDateTime": "2018-09-05T00:11:27.773602Z",
    "userId": "abcdefab-af90-4edf-ac4c-742ff06735d0",
    "userDisplayName": "Olivia Lack",
    "userPrincipalName": "olack@adatum.com",
    "additionalInfo": "[{\"Key\":\"userAgent\",\"Value\":\"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/68.0.3440.106 Safari/537.36\"}]"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get riskDetection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

