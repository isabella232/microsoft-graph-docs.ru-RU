---
title: Список Транситивемембероф
description: Получение групп, участником которых является контакт органзиатионал. Этот запрос API является транзитивным и также возвращает все группы, в которых пользователь является вложенным.
author: anchanda
localization_priority: Normal
ms.prod: groups
doc_type: apiPageType
ms.openlocfilehash: 97f787dad12e499b64d43714e3cbe7b27be36d39
ms.sourcegitcommit: c9b9ff2c862f8d96d282a7bdf641cdb9c53a4600
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2019
ms.locfileid: "37633906"
---
# <a name="list-transitivememberof"></a><span data-ttu-id="4c2c3-104">Список Транситивемембероф</span><span class="sxs-lookup"><span data-stu-id="4c2c3-104">List transitiveMemberOf</span></span>

<span data-ttu-id="4c2c3-105">Получение групп, членом которых является это [организационное Контактное лицо](../resources/orgcontact.md) .</span><span class="sxs-lookup"><span data-stu-id="4c2c3-105">Get groups that this [organizational contact](../resources/orgcontact.md) is a member of.</span></span> <span data-ttu-id="4c2c3-106">Запрос API является транзитивным и возвращает все группы. Контактное лицо является вложенным элементом.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-106">The API request is transitive, and returns all groups the organizational contact is a nested member of.</span></span>

## <a name="permissions"></a><span data-ttu-id="4c2c3-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4c2c3-107">Permissions</span></span>

<span data-ttu-id="4c2c3-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4c2c3-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4c2c3-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="4c2c3-110">Permission type</span></span>      | <span data-ttu-id="4c2c3-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="4c2c3-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4c2c3-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="4c2c3-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4c2c3-113">OrgContact. Read. ALL и Group. Read. ALL, Directory. Read. ALL</span><span class="sxs-lookup"><span data-stu-id="4c2c3-113">OrgContact.Read.All and Group.Read.All, Directory.Read.All</span></span>  |
|<span data-ttu-id="4c2c3-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="4c2c3-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4c2c3-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-115">Not supported.</span></span>    |
|<span data-ttu-id="4c2c3-116">Для приложения</span><span class="sxs-lookup"><span data-stu-id="4c2c3-116">Application</span></span> | <span data-ttu-id="4c2c3-117">OrgContact. Read. ALL и Group. Read. ALL, Directory. Read. ALL</span><span class="sxs-lookup"><span data-stu-id="4c2c3-117">OrgContact.Read.All and Group.Read.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4c2c3-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="4c2c3-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /contacts/{id}/transitiveMemberOf
```

## <a name="optional-query-parameters"></a><span data-ttu-id="4c2c3-119">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="4c2c3-119">Optional query parameters</span></span>

<span data-ttu-id="4c2c3-120">Этот метод поддерживает `$select` [параметры запросов OData](/graph/query-parameters) для настройки отклика.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-120">This method supports the `$select` [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4c2c3-121">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="4c2c3-121">Request headers</span></span>

| <span data-ttu-id="4c2c3-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4c2c3-122">Header</span></span>       | <span data-ttu-id="4c2c3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4c2c3-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4c2c3-124">Авторизация</span><span class="sxs-lookup"><span data-stu-id="4c2c3-124">Authorization</span></span>  | <span data-ttu-id="4c2c3-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="4c2c3-127">Accept</span><span class="sxs-lookup"><span data-stu-id="4c2c3-127">Accept</span></span>  | <span data-ttu-id="4c2c3-128">application/json</span><span class="sxs-lookup"><span data-stu-id="4c2c3-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4c2c3-129">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="4c2c3-129">Request body</span></span>

<span data-ttu-id="4c2c3-130">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4c2c3-131">Отклик</span><span class="sxs-lookup"><span data-stu-id="4c2c3-131">Response</span></span>

<span data-ttu-id="4c2c3-132">В случае успеха этот метод возвращает код отклика `200 OK` и коллекцию объектов [directoryObject](../resources/directoryobject.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-132">If successful, this method returns a `200 OK` response code and a collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4c2c3-133">Пример</span><span class="sxs-lookup"><span data-stu-id="4c2c3-133">Example</span></span>

### <a name="request"></a><span data-ttu-id="4c2c3-134">Запрос</span><span class="sxs-lookup"><span data-stu-id="4c2c3-134">Request</span></span>

<span data-ttu-id="4c2c3-135">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-135">The following is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="4c2c3-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="4c2c3-136">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "orgcontact_list_transitivememberof"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/me/transitiveMemberOf
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="4c2c3-137">C#</span><span class="sxs-lookup"><span data-stu-id="4c2c3-137">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/orgcontact-list-transitivememberof-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="4c2c3-138">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4c2c3-138">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/orgcontact-list-transitivememberof-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="4c2c3-139">Objective-C</span><span class="sxs-lookup"><span data-stu-id="4c2c3-139">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/orgcontact-list-transitivememberof-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="4c2c3-140">Java</span><span class="sxs-lookup"><span data-stu-id="4c2c3-140">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/orgcontact-list-transitivememberof-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="4c2c3-141">Отклик</span><span class="sxs-lookup"><span data-stu-id="4c2c3-141">Response</span></span>

<span data-ttu-id="4c2c3-142">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-142">The following is an example of the response.</span></span>
><span data-ttu-id="4c2c3-143">**Примечание**. Объект отклика, показанный здесь, может быть сокращен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-143">**Note**: The response object shown here might be shortened for readability.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.group",
      "id": "id-value",
      "createdDateTime": null,
      "description": "All users at the company",
      "displayName": "All Users",
      "groupTypes": [],
      "mailEnabled": false,
      "securityEnabled": true,
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List orgContact transitiveMemberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->