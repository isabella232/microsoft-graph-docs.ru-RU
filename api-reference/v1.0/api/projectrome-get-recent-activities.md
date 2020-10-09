---
title: Получение последних действий пользователя
description: " Функцию. Служба будет запрашивать последние Historyitem, а затем извлекать эти связанные действия. Действия сортируются в соответствии с последним значением **LastModified** в **historyItem**. Это означает, что действия без **historyitem** не будут включены в ответ. Разрешение UserActivity. ReadWrite. CreatedByApp также будет применять к отклику дополнительную фильтрацию, чтобы возвращались только действия, созданные приложением. Такая фильтрация на стороне сервера может привести к пустым страницам, если пользователь является особенно активным и другие приложения создали более новые действия. Чтобы получить действия приложения, используйте свойство **nextLink** для разбивки на страницы."
localization_priority: Normal
ms.prod: project-rome
author: ailae
doc_type: apiPageType
ms.openlocfilehash: 459de1d6309f8db37180cd99e3286974bfd8c373
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "48405892"
---
# <a name="get-recent-user-activities"></a><span data-ttu-id="dd283-109">Получение последних действий пользователя</span><span class="sxs-lookup"><span data-stu-id="dd283-109">Get recent user activities</span></span>

<span data-ttu-id="dd283-110">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="dd283-110">Namespace: microsoft.graph</span></span>

<span data-ttu-id="dd283-111">Получение последних действий для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="dd283-111">Get recent activities for a given user.</span></span> <span data-ttu-id="dd283-112">Эта функция OData имеет некоторые варианты поведения по умолчанию, которые могут работать так же, как и "самый последний использованный" API.</span><span class="sxs-lookup"><span data-stu-id="dd283-112">This OData function has some default behaviors included to make it operate like a "most recently used" API.</span></span> <span data-ttu-id="dd283-113">Служба будет запрашивать последние [historyitem](../resources/projectrome-historyitem.md), а затем извлекать эти связанные действия.</span><span class="sxs-lookup"><span data-stu-id="dd283-113">The service will query for the most recent [historyItems](../resources/projectrome-historyitem.md), and then pull those related activities.</span></span> <span data-ttu-id="dd283-114">Действия сортируются в соответствии с последним значением **LastModified** в **historyItem**.</span><span class="sxs-lookup"><span data-stu-id="dd283-114">Activities will be sorted according to the most recent **lastModified** on the **historyItem**.</span></span> <span data-ttu-id="dd283-115">Это означает, что действия без **historyitem** не будут включены в ответ.</span><span class="sxs-lookup"><span data-stu-id="dd283-115">This means that activities without **historyItems** will not be included in the response.</span></span> <span data-ttu-id="dd283-116">Разрешение UserActivity. ReadWrite. CreatedByApp также будет применять к отклику дополнительную фильтрацию, чтобы возвращались только действия, созданные приложением.</span><span class="sxs-lookup"><span data-stu-id="dd283-116">The UserActivity.ReadWrite.CreatedByApp permission will also apply extra filtering to the response, so that only activities created by your application are returned.</span></span> <span data-ttu-id="dd283-117">Такая фильтрация на стороне сервера может привести к пустым страницам, если пользователь является особенно активным и другие приложения создали более новые действия.</span><span class="sxs-lookup"><span data-stu-id="dd283-117">This server-side filtering might result in empty pages if the user is particularly active and other applications have created more recent activities.</span></span> <span data-ttu-id="dd283-118">Чтобы получить действия приложения, используйте свойство **nextLink** для разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="dd283-118">To get your application's activities, use the **nextLink** property to paginate.</span></span>

## <a name="permissions"></a><span data-ttu-id="dd283-119">Разрешения</span><span class="sxs-lookup"><span data-stu-id="dd283-119">Permissions</span></span>

<span data-ttu-id="dd283-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dd283-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dd283-122">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="dd283-122">Permission type</span></span>      | <span data-ttu-id="dd283-123">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="dd283-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dd283-124">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="dd283-124">Delegated (work or school account)</span></span> | <span data-ttu-id="dd283-125">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="dd283-125">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="dd283-126">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="dd283-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dd283-127">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="dd283-127">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="dd283-128">Для приложений</span><span class="sxs-lookup"><span data-stu-id="dd283-128">Application</span></span> | <span data-ttu-id="dd283-129">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dd283-129">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dd283-130">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="dd283-130">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/activities/recent
```

## <a name="optional-query-parameters"></a><span data-ttu-id="dd283-131">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="dd283-131">Optional query parameters</span></span>

<span data-ttu-id="dd283-132">Этот метод поддерживает некоторые [Параметры запроса OData](/graph/query-parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="dd283-132">This method supports some [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span> <span data-ttu-id="dd283-133">Поддерживаются следующие параметры запросов:</span><span class="sxs-lookup"><span data-stu-id="dd283-133">The following query parameters are supported:</span></span>

- <span data-ttu-id="dd283-134">$expand для свойства навигации **historyitem** .</span><span class="sxs-lookup"><span data-stu-id="dd283-134">$expand for the **historyItems** navigation property.</span></span>
- <span data-ttu-id="dd283-135">$top, чтобы ограничить максимальное количество элементов на страницах.</span><span class="sxs-lookup"><span data-stu-id="dd283-135">$top to limit the maximum number of items across pages.</span></span>
- <span data-ttu-id="dd283-136">$filter в свойстве **lastModifiedDateTime** для **действий** или **historyitem**, если она развернута.</span><span class="sxs-lookup"><span data-stu-id="dd283-136">$filter on the **lastModifiedDateTime** property for either **activities** or **historyItems**, if expanded.</span></span>

<span data-ttu-id="dd283-137">Ниже приведено несколько примеров поддерживаемых запросов с кодированием URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="dd283-137">The following are some examples of supported queries with URL encoding.</span></span>

```
/me/activities/recent?$expand=historyItems($filter=lastModifiedDateTime%20gt%202018-01-22T21:45:00.347Z%20and%20lastModifiedDateTime%20lt%202018-01-22T22:00:00.347Z)

/me/activities/recent?$filter=lastModifiedDateTime%20lt%202018-01-16T01:03:21.347Z%20and%20lastModifiedDateTime%20gt%202018-01-03T01:03:21.347Z

/me/activities/recent?$top=5
```

## <a name="request-headers"></a><span data-ttu-id="dd283-138">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="dd283-138">Request headers</span></span>

|<span data-ttu-id="dd283-139">Имя</span><span class="sxs-lookup"><span data-stu-id="dd283-139">Name</span></span> | <span data-ttu-id="dd283-140">Тип</span><span class="sxs-lookup"><span data-stu-id="dd283-140">Type</span></span> | <span data-ttu-id="dd283-141">Описание</span><span class="sxs-lookup"><span data-stu-id="dd283-141">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="dd283-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="dd283-142">Authorization</span></span> | <span data-ttu-id="dd283-143">string</span><span class="sxs-lookup"><span data-stu-id="dd283-143">string</span></span> | <span data-ttu-id="dd283-p105">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="dd283-p105">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="dd283-146">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="dd283-146">Request body</span></span>

<span data-ttu-id="dd283-147">Не указывайте текст запроса.</span><span class="sxs-lookup"><span data-stu-id="dd283-147">Do not specify a request body.</span></span>

## <a name="response"></a><span data-ttu-id="dd283-148">Отклик</span><span class="sxs-lookup"><span data-stu-id="dd283-148">Response</span></span>

<span data-ttu-id="dd283-149">В случае успешного выполнения этот метод возвращает `200 OK` код отклика с последними действиями пользователя для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="dd283-149">If successful, this method returns the `200 OK` response code with the user's recent activities for your application.</span></span>

## <a name="example"></a><span data-ttu-id="dd283-150">Пример</span><span class="sxs-lookup"><span data-stu-id="dd283-150">Example</span></span>

##### <a name="request"></a><span data-ttu-id="dd283-151">Запрос</span><span class="sxs-lookup"><span data-stu-id="dd283-151">Request</span></span>

<span data-ttu-id="dd283-152">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="dd283-152">The following is an example of the request.</span></span>


# <a name="http"></a>[<span data-ttu-id="dd283-153">HTTP</span><span class="sxs-lookup"><span data-stu-id="dd283-153">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_recent_activities"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/me/activities/recent
```
# <a name="c"></a>[<span data-ttu-id="dd283-154">C#</span><span class="sxs-lookup"><span data-stu-id="dd283-154">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-recent-activities-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="dd283-155">JavaScript</span><span class="sxs-lookup"><span data-stu-id="dd283-155">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-recent-activities-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="dd283-156">Objective-C</span><span class="sxs-lookup"><span data-stu-id="dd283-156">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-recent-activities-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="dd283-157">Java</span><span class="sxs-lookup"><span data-stu-id="dd283-157">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-recent-activities-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="dd283-158">Отклик</span><span class="sxs-lookup"><span data-stu-id="dd283-158">Response</span></span>

<span data-ttu-id="dd283-159">Ниже приведен пример ответа.</span><span class="sxs-lookup"><span data-stu-id="dd283-159">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.userActivity)"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(userActivity)",
    "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/activities/recent?$skiptoken=%24filter%3dlastModifiedDateTime+lt+2018-02-26T18%3a06%3a19.365Z",
    "value": [{
        "@odata.type": "#microsoft.graph.userActivity",
        "activitySourceHost": "https://www.contoso.com",
        "createdDateTime": "2018-02-26T18:34:29.592Z",
        "lastModifiedDateTime": "2018-02-26T18:34:29.607Z",
        "id": "5347642601316252694",
        "appActivityId": "/article?12345",
        "visualElements": {
            "attribution": {
              "iconUrl": "https://www.contoso.com/icon",
              "alternateText": "Contoso, Ltd.",
              "addImageQuery": false,
              },
            "displayText": "Contoso How-To: How to Tie a Reef Knot",
            "description": "How to Tie a Reef Knot. A step-by-step visual guide to the art of nautical knot-tying.",
            "backgroundColor": "#ff0000",
            "content": {
              "$schema": "https://adaptivecards.io/schemas/adaptive-card.json",
              "type": "AdaptiveCard",
              "body":
              [{
                  "type": "TextBlock",
                  "text": "Contoso MainPage"
              }]
            }
        },
        "activationUrl": "https://www.contoso.com/article?id=12345",
        "appDisplayName": "Contoso, Ltd.",
        "userTimezone": "Africa/Casablanca",
        "fallbackUrl": "https://www.contoso.com/article?id=12345",
        "contentUrl": "https://www.contoso.com/article?id=12345",
        "contentInfo": {
            "@context": "https://schema.org",
            "@type": "Article",
            "author": "John Doe",
            "name": "How to Tie a Reef Knot"
        },
        "expirationDateTime": "2018-03-28T18:34:29.607Z",
        "status": "updated"
    }]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get recent activities",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Error: get_recent_activities/container/contentInfo:
      Property 'contentInfo' is of type Custom but has no custom members.",

    "Warning: get_recent_activities/container/visualElements/content/$schema:
      Undocumented property '$schema' [String] was not expected on resource microsoft.graph.Json.",

    "Warning: get_recent_activities/container/visualElements/content/body:
      Undocumented property 'body' [Collection(Object)] was not expected on resource microsoft.graph.Json.",

    "Warning: get_recent_activities/container/visualElements/content/type:
      Undocumented property 'type' [String] was not expected on resource microsoft.graph.Json."

  ],
  "tocPath": ""
}-->