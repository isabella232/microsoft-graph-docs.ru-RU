---
title: Получение Аппликатионсигнинсуммари
description: Получение свойств и связей объекта **аппликатионсигнинсуммари** .
localization_priority: Normal
author: dhanyahk
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: c7b085b8142c8f2bd2a2a0b0f502178a7179a398
ms.sourcegitcommit: d6386c5d4bb8917132c3f6c4de945487939b7fb7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "43107047"
---
# <a name="get-applicationsigninsummary"></a><span data-ttu-id="b74a8-103">Получение Аппликатионсигнинсуммари</span><span class="sxs-lookup"><span data-stu-id="b74a8-103">Get applicationSignInSummary</span></span>

<span data-ttu-id="b74a8-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="b74a8-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="b74a8-105">Получение свойств и связей объекта [аппликатионсигнинсуммари](../resources/applicationsigninsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="b74a8-105">Retrieve the properties and relationships of an [applicationSigninSummary](../resources/applicationsigninsummary.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="b74a8-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="b74a8-106">Permissions</span></span>
<span data-ttu-id="b74a8-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b74a8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference.md).</span></span>

|<span data-ttu-id="b74a8-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="b74a8-109">Permission type</span></span>      | <span data-ttu-id="b74a8-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="b74a8-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b74a8-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b74a8-111">Delegated (work or school account)</span></span> | <span data-ttu-id="b74a8-112">Report. Read. ALL</span><span class="sxs-lookup"><span data-stu-id="b74a8-112">Report.Read.All</span></span> |
|<span data-ttu-id="b74a8-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="b74a8-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b74a8-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b74a8-114">Not supported</span></span>   |
|<span data-ttu-id="b74a8-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="b74a8-115">Application</span></span> | <span data-ttu-id="b74a8-116">Report. Read. ALL</span><span class="sxs-lookup"><span data-stu-id="b74a8-116">Report.Read.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="b74a8-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="b74a8-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
``` http
GET reports/getAzureADApplicationSignInSummary(period='{period}')
```

## <a name="function-parameters"></a><span data-ttu-id="b74a8-118">Параметры функции</span><span class="sxs-lookup"><span data-stu-id="b74a8-118">Function parameters</span></span>

| <span data-ttu-id="b74a8-119">Параметр</span><span class="sxs-lookup"><span data-stu-id="b74a8-119">Parameter</span></span> | <span data-ttu-id="b74a8-120">Описание</span><span class="sxs-lookup"><span data-stu-id="b74a8-120">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="b74a8-121">period</span><span class="sxs-lookup"><span data-stu-id="b74a8-121">period</span></span> | <span data-ttu-id="b74a8-122">Либо `D7` (последние семь дней), `D30` либо (последние 30 дней); другие значения создают ошибки.</span><span class="sxs-lookup"><span data-stu-id="b74a8-122">Either `D7` (last seven days) or `D30` (last 30 days); other values generate errors.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="b74a8-123">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="b74a8-123">Request headers</span></span>
| <span data-ttu-id="b74a8-124">Имя</span><span class="sxs-lookup"><span data-stu-id="b74a8-124">Name</span></span>      |<span data-ttu-id="b74a8-125">Описание</span><span class="sxs-lookup"><span data-stu-id="b74a8-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="b74a8-126">Авторизация</span><span class="sxs-lookup"><span data-stu-id="b74a8-126">Authorization</span></span> | <span data-ttu-id="b74a8-127">Bearer {code}</span><span class="sxs-lookup"><span data-stu-id="b74a8-127">Bearer {code}</span></span> |

## <a name="request-body"></a><span data-ttu-id="b74a8-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="b74a8-128">Request body</span></span>
<span data-ttu-id="b74a8-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="b74a8-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b74a8-130">Ответ</span><span class="sxs-lookup"><span data-stu-id="b74a8-130">Response</span></span>
<span data-ttu-id="b74a8-131">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и объект [аппликатионсигнинсуммари](../resources/applicationsigninsummary.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="b74a8-131">If successful, this method returns a `200 OK` response code and an [applicationSignInSummary](../resources/applicationsigninsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b74a8-132">Пример</span><span class="sxs-lookup"><span data-stu-id="b74a8-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="b74a8-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="b74a8-133">Request</span></span>
<span data-ttu-id="b74a8-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="b74a8-134">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="b74a8-135">HTTP</span><span class="sxs-lookup"><span data-stu-id="b74a8-135">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_applicationsigninsummary"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/reports/getAzureADApplicationSignInSummary(period='D7')
```
# <a name="c"></a>[<span data-ttu-id="b74a8-136">C#</span><span class="sxs-lookup"><span data-stu-id="b74a8-136">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-applicationsigninsummary-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="b74a8-137">JavaScript</span><span class="sxs-lookup"><span data-stu-id="b74a8-137">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-applicationsigninsummary-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="b74a8-138">Objective-C</span><span class="sxs-lookup"><span data-stu-id="b74a8-138">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-applicationsigninsummary-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### <a name="response"></a><span data-ttu-id="b74a8-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="b74a8-139">Response</span></span>
<span data-ttu-id="b74a8-140">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="b74a8-140">The following is an example of the response.</span></span> 

><span data-ttu-id="b74a8-141">**Примечание:** Объект Response, показанный здесь, ммигхт должен быть укорочен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="b74a8-141">**Note:** The response object shown here mmight be shortened for readability.</span></span> <span data-ttu-id="b74a8-142">При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="b74a8-142">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.applicationSignInSummary"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 157

{
  "appId": "appId-value",
  "appDisplayName": "appDisplayName-value",
  "successfulSignInCount": 99,
  "failedSignInCount": 99,
  "successPercentage": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get applicationSignInSummary",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
