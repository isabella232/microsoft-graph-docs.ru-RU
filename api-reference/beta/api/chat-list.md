---
title: Список чатов
description: Получение списка бесед для пользователя.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: 46afd5b3cc76c9df74cce5d26c13d6af28382d13
ms.sourcegitcommit: 87966dcd42a0111c5c9987fcae0a491c92022938
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "44287642"
---
# <a name="list-chats"></a><span data-ttu-id="227c5-103">Список чатов</span><span class="sxs-lookup"><span data-stu-id="227c5-103">List chats</span></span>

<span data-ttu-id="227c5-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="227c5-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="227c5-105">Получение списка [сеансов](../resources/chat.md) , в которые входит пользователь.</span><span class="sxs-lookup"><span data-stu-id="227c5-105">Retrieve the list of [chats](../resources/chat.md) that the user is part of.</span></span>

## <a name="permissions"></a><span data-ttu-id="227c5-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="227c5-106">Permissions</span></span>

<span data-ttu-id="227c5-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="227c5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="227c5-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="227c5-109">Permission type</span></span>      | <span data-ttu-id="227c5-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="227c5-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="227c5-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="227c5-111">Delegated (work or school account)</span></span> | <span data-ttu-id="227c5-112">Чат. ReadBasic, Chat. Read, Chat. ReadWrite</span><span class="sxs-lookup"><span data-stu-id="227c5-112">Chat.ReadBasic, Chat.Read, Chat.ReadWrite</span></span> |
|<span data-ttu-id="227c5-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="227c5-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="227c5-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="227c5-114">Not supported.</span></span>    |
|<span data-ttu-id="227c5-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="227c5-115">Application</span></span> | <span data-ttu-id="227c5-116">Chat. ReadBasic. ALL, Chat. Read. ALL, Chat. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="227c5-116">Chat.ReadBasic.All, Chat.Read.All, Chat.ReadWrite.All</span></span> | 

> [!NOTE]
> <span data-ttu-id="227c5-117">Перед вызовом этого API с разрешениями приложения необходимо запросить доступ.</span><span class="sxs-lookup"><span data-stu-id="227c5-117">Before calling this API with application permissions, you must request access.</span></span> <span data-ttu-id="227c5-118">Дополнительные сведения см. в статье [Защищенные APIs в Microsoft Teams](/graph/teams-protected-apis).</span><span class="sxs-lookup"><span data-stu-id="227c5-118">For details, see [Protected APIs in Microsoft Teams](/graph/teams-protected-apis).</span></span>

## <a name="http-request"></a><span data-ttu-id="227c5-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="227c5-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/chats
GET /users/{id}/chats
GET /chats
```

## <a name="optional-query-parameters"></a><span data-ttu-id="227c5-120">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="227c5-120">Optional query parameters</span></span>

<span data-ttu-id="227c5-121">Это действие в настоящее время не поддерживает [параметры запросов OData](/graph/query-parameters) для настройки отклика.</span><span class="sxs-lookup"><span data-stu-id="227c5-121">This operation does not currently support [OData query parameters](/graph/query-parameters) to customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="227c5-122">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="227c5-122">Request headers</span></span>

| <span data-ttu-id="227c5-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="227c5-123">Header</span></span>       | <span data-ttu-id="227c5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="227c5-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="227c5-125">Авторизация</span><span class="sxs-lookup"><span data-stu-id="227c5-125">Authorization</span></span>  | <span data-ttu-id="227c5-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="227c5-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="227c5-128">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="227c5-128">Request body</span></span>

<span data-ttu-id="227c5-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="227c5-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="227c5-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="227c5-130">Response</span></span>

<span data-ttu-id="227c5-131">При успешном выполнении этот метод возвращает код отклика `200 OK` и коллекцию объектов [chat](../resources/chat.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="227c5-131">If successful, this method returns a `200 OK` response code and a collection of [chat](../resources/chat.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="227c5-132">Пример</span><span class="sxs-lookup"><span data-stu-id="227c5-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="227c5-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="227c5-133">Request</span></span>

<span data-ttu-id="227c5-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="227c5-134">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="227c5-135">HTTP</span><span class="sxs-lookup"><span data-stu-id="227c5-135">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_chats"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/users/{id}/chats
```
# <a name="c"></a>[<span data-ttu-id="227c5-136">C#</span><span class="sxs-lookup"><span data-stu-id="227c5-136">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-chats-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="227c5-137">JavaScript</span><span class="sxs-lookup"><span data-stu-id="227c5-137">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-chats-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="227c5-138">Objective-C</span><span class="sxs-lookup"><span data-stu-id="227c5-138">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-chats-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="227c5-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="227c5-139">Response</span></span>

<span data-ttu-id="227c5-140">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="227c5-140">Here is an example of the response.</span></span> 

><span data-ttu-id="227c5-p104">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="227c5-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chat",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 262

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#chats",
    "value": [
        {
            "id": "19:8b081ef6-4792-4def-b2c9-c363a1bf41d5_877192bd-9183-47d3-a74c-8aa0426716cf@unq.gbl.spaces",
            "topic": null,
            "createdDateTime": "2019-04-18T23:51:42.099Z",
            "lastUpdatedDateTime": "2019-04-18T23:51:43.255Z"
        },
        {
            "id": "19:8b081ef6-4792-4def-b2c9-c363a1bf41d5_0c5cfdbb-596f-4d39-b557-5d9516c94107@unq.gbl.spaces",
            "topic": null,
            "createdDateTime": "2019-04-18T23:19:23.76Z",
            "lastUpdatedDateTime": "2019-04-18T23:19:21.994Z"
        },
        {
            "id": "19:8b081ef6-4792-4def-b2c9-c363a1bf41d5_3ee373aa-62fa-4fc6-b11f-9627d5b4a73d@unq.gbl.spaces",
            "topic": null,
            "createdDateTime": "2019-03-21T22:30:14.867Z",
            "lastUpdatedDateTime": "2019-03-21T22:30:15.507Z"
        },
        {
            "id": "19:8b081ef6-4792-4def-b2c9-c363a1bf41d5_90a27c51-5c74-453b-944a-134ba86da790@unq.gbl.spaces",
            "topic": null,
            "createdDateTime": "2019-02-06T03:38:58.062Z",
            "lastUpdatedDateTime": "2019-02-06T03:38:58.063Z"
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "List chats",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
