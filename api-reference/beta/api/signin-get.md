---
title: Получение вход
description: Извлекает Azure AD входы для клиента. Войти в систему, взаимодействующих в характер (где имя пользователя и пароль передается как часть маркера авторизации) и успешные федеративных войти в систему в данный момент включены в журналы входа.
ms.openlocfilehash: 1934af9b918dc976ef7f3fc6cdd21c04f6fcc705
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27081048"
---
# <a name="get-signin"></a><span data-ttu-id="d6346-104">Получение вход</span><span class="sxs-lookup"><span data-stu-id="d6346-104">Get signIn</span></span>
<span data-ttu-id="d6346-105">Извлекает Azure AD входы для клиента.</span><span class="sxs-lookup"><span data-stu-id="d6346-105">Retrieves the Azure AD user sign-ins for your tenant.</span></span> <span data-ttu-id="d6346-106">Войти в систему, взаимодействующих в характер (где имя пользователя и пароль передается как часть маркера авторизации) и успешные федеративных войти в систему в данный момент включены в журналы входа.</span><span class="sxs-lookup"><span data-stu-id="d6346-106">Sign-ins that are interactive in nature (where a username/password is passed as part of authorization token) and successful federated sign-ins are currently included in the sign-in logs.</span></span>


## <a name="permissions"></a><span data-ttu-id="d6346-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="d6346-107">Permissions</span></span>
<span data-ttu-id="d6346-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d6346-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d6346-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="d6346-110">Permission type</span></span>      | <span data-ttu-id="d6346-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="d6346-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d6346-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d6346-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d6346-113">AuditLog.Read.All</span><span class="sxs-lookup"><span data-stu-id="d6346-113">AuditLog.Read.All</span></span> |
|<span data-ttu-id="d6346-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="d6346-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d6346-115">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d6346-115">Not supported</span></span>   |
|<span data-ttu-id="d6346-116">Для приложения</span><span class="sxs-lookup"><span data-stu-id="d6346-116">Application</span></span> | <span data-ttu-id="d6346-117">AuditLog.Read.All</span><span class="sxs-lookup"><span data-stu-id="d6346-117">AuditLog.Read.All</span></span> | 

<span data-ttu-id="d6346-118">Кроме того приложения должны быть [правильно зарегистрирован](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-prerequisites-azure-portal) для Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d6346-118">In addition, apps must be [properly registered](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-prerequisites-azure-portal) to Azure AD.</span></span>

## <a name="http-request"></a><span data-ttu-id="d6346-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="d6346-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /auditLogs/signIns/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d6346-120">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="d6346-120">Optional query parameters</span></span>
<span data-ttu-id="d6346-121">Этот метод поддерживает следующие параметры запроса OData для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="d6346-121">This method supports the following OData Query Parameters to help customize the response.</span></span> <span data-ttu-id="d6346-122">Проверьте [Параметры запроса OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для порядок использования этих параметров.</span><span class="sxs-lookup"><span data-stu-id="d6346-122">Check [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) for how to use these parameters.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d6346-123">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="d6346-123">Request headers</span></span>
| <span data-ttu-id="d6346-124">Имя</span><span class="sxs-lookup"><span data-stu-id="d6346-124">Name</span></span>      |<span data-ttu-id="d6346-125">Описание</span><span class="sxs-lookup"><span data-stu-id="d6346-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d6346-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="d6346-126">Authorization</span></span>  | <span data-ttu-id="d6346-127">Bearer {code}</span><span class="sxs-lookup"><span data-stu-id="d6346-127">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="d6346-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="d6346-128">Request body</span></span>
<span data-ttu-id="d6346-129">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="d6346-129">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="d6346-130">Ответ</span><span class="sxs-lookup"><span data-stu-id="d6346-130">Response</span></span>
<span data-ttu-id="d6346-131">Успешно завершена, этот метод возвращает `200 OK` объект [входить](../resources/signin.md) и кода ответа в теле ответа.</span><span class="sxs-lookup"><span data-stu-id="d6346-131">If successful, this method returns a `200 OK` response code and [signIn](../resources/signin.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d6346-132">Пример</span><span class="sxs-lookup"><span data-stu-id="d6346-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d6346-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="d6346-133">Request</span></span>
<span data-ttu-id="d6346-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="d6346-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "reque|location/city| eq, startswith|
st",
  "name": "get_signin"
}-->
```http
GET https://graph.microsoft.com/beta/auditLogs/signIns/{id}
```
##### <a name="response"></a><span data-ttu-id="d6346-135">Ответ</span><span class="sxs-lookup"><span data-stu-id="d6346-135">Response</span></span>
<span data-ttu-id="d6346-136">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="d6346-136">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.signIn"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 211
```
```json
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#auditLogs/signIns",
    "value": [{
        "id": "id",
        "createdDateTime": "2018-01-09T21:17:21.5077253Z",
        "userDisplayName": "Jamie Doe",
        "userPrincipalName": "jdoe@contoso.com",
        "userId": "bbb3b4b5-e6e6-f7f5-f7f5-090805040302",
        "appId": "d3590ed6-52b3-4102-aeff-aad2292ab01c",
        "appDisplayName": "Azure",
        "ipAddress": "127.0.0.1",
        "status": {
            "errorCode": 0,
            "failureReason": null,
            "additionalDetails": "SignIn Success & CA Sucess"
        },
        "clientAppUsed": null,
        "deviceDetail": {
            "deviceId": "34390ed6-52b3-4102-aeff-aad2292abac3",
            "displayName": "DeviceName",
            "operatingSystem": "Windows 10",
            "browser": "Rich Client v1.0.2016.0",
            "isCompliant": true,
            "isManaged": true,
            "trustType": ""
        },
        "location": {
            "city": "Redmond",
            "state": "WA",
            "countryOrRegion": "USA",
            "geoCoordinates": {
                "altitude": 41.589,
                "latitude": 41.589,
                "longitude": -93.6151
            }
        },
        "mfaDetail": {
            "mfaAuthMethod": "Phone Auth",
            "mfaAuthDetail": null
        },
        "correlationId": "17c47d3c-593d-4d08-ac20-813892b87e42",
        "conditionalAccessApplied": true,
        "conditionalAccessPolicies": [{
            "id": "26490ed6-52b3-4102-aeff-aad2292abacf",
            "displayName": "capPolicy",
            "enforcedAccessControls": ["MFA", "TOU"],
            "enforcedSessionControls": ["CloudAppSecurity"],
            "result": "success"
        }],
        "isRisky": false,
        "riskLevel": "low"
    }]
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get signIn",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->