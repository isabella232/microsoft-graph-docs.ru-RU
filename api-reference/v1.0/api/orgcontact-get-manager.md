---
title: Получение имени руководителя
description: Получение руководителя этого контакта в Организации.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: c29f3912280faef09753d89be148c9f93e350053
ms.sourcegitcommit: c9b9ff2c862f8d96d282a7bdf641cdb9c53a4600
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2019
ms.locfileid: "37633996"
---
# <a name="get-manager"></a><span data-ttu-id="dc33e-103">Получение имени руководителя</span><span class="sxs-lookup"><span data-stu-id="dc33e-103">Get manager</span></span>

<span data-ttu-id="dc33e-104">Получение руководителя этого контакта в Организации.</span><span class="sxs-lookup"><span data-stu-id="dc33e-104">Get this organizational contact's manager.</span></span>

## <a name="permissions"></a><span data-ttu-id="dc33e-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="dc33e-105">Permissions</span></span>
<span data-ttu-id="dc33e-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc33e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dc33e-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="dc33e-108">Permission type</span></span>      | <span data-ttu-id="dc33e-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="dc33e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dc33e-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="dc33e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="dc33e-111">OrgContact. Read. ALL и Group. Read. ALL, Directory. Read. ALL</span><span class="sxs-lookup"><span data-stu-id="dc33e-111">OrgContact.Read.All and Group.Read.All, Directory.Read.All</span></span>   |
|<span data-ttu-id="dc33e-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="dc33e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dc33e-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc33e-113">Not supported.</span></span>    |
|<span data-ttu-id="dc33e-114">Для приложения</span><span class="sxs-lookup"><span data-stu-id="dc33e-114">Application</span></span> | <span data-ttu-id="dc33e-115">OrgContact. Read. ALL и Group. Read. ALL, Directory. Read. ALL</span><span class="sxs-lookup"><span data-stu-id="dc33e-115">OrgContact.Read.All and Group.Read.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="dc33e-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="dc33e-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /contacts/{id}/manager
```

## <a name="optional-query-parameters"></a><span data-ttu-id="dc33e-117">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="dc33e-117">Optional query parameters</span></span>
<span data-ttu-id="dc33e-118">Этот метод поддерживает `$select` [параметры запросов OData](/graph/query-parameters) для настройки отклика.</span><span class="sxs-lookup"><span data-stu-id="dc33e-118">This method supports the `$select` [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="dc33e-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="dc33e-119">Request headers</span></span>
| <span data-ttu-id="dc33e-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dc33e-120">Header</span></span>       | <span data-ttu-id="dc33e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="dc33e-121">Value</span></span> |
|:-----------|:----------|
| <span data-ttu-id="dc33e-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="dc33e-122">Authorization</span></span>  | <span data-ttu-id="dc33e-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="dc33e-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dc33e-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="dc33e-125">Request body</span></span>
<span data-ttu-id="dc33e-126">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="dc33e-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dc33e-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="dc33e-127">Response</span></span>

<span data-ttu-id="dc33e-128">В случае успеха этот метод возвращает код отклика `200 OK` и коллекцию объектов [directoryObject](../resources/directoryobject.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="dc33e-128">If successful, this method returns a `200 OK` response code and a collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="dc33e-129">Пример</span><span class="sxs-lookup"><span data-stu-id="dc33e-129">Example</span></span>

#### <a name="request"></a><span data-ttu-id="dc33e-130">Запрос</span><span class="sxs-lookup"><span data-stu-id="dc33e-130">Request</span></span>


# <a name="httptabhttp"></a>[<span data-ttu-id="dc33e-131">HTTP</span><span class="sxs-lookup"><span data-stu-id="dc33e-131">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_manager"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/contacts/{id}/manager
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="dc33e-132">C#</span><span class="sxs-lookup"><span data-stu-id="dc33e-132">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-manager-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="dc33e-133">JavaScript</span><span class="sxs-lookup"><span data-stu-id="dc33e-133">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-manager-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="dc33e-134">Objective-C</span><span class="sxs-lookup"><span data-stu-id="dc33e-134">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-manager-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="dc33e-135">Java</span><span class="sxs-lookup"><span data-stu-id="dc33e-135">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-manager-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a><span data-ttu-id="dc33e-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="dc33e-136">Response</span></span>
<span data-ttu-id="dc33e-137">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="dc33e-137">The following is an example of the response.</span></span>
><span data-ttu-id="dc33e-138">**Примечание**. Объект отклика, показанный здесь, может быть сокращен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="dc33e-138">**Note**: The response object shown here might be shortened for readability.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": false
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 455

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#directoryObjects/$entity",
    "@odata.type": "#microsoft.graph.user",
    "id": "24fcbca3-c3e2-48bf-9ffc-c7f81b81483d",
    "businessPhones": [
        "+1 205 555 0108"
    ],
    "displayName": "Diego Siciliani",
    "givenName": "Diego",
    "jobTitle": "CVP Finance",
    "mail": "DiegoS@contoso.com",
    "mobilePhone": null,
    "officeLocation": "14/1108",
    "preferredLanguage": "en-US",
    "surname": "Siciliani",
    "userPrincipalName": "DiegoS@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Get manager",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->