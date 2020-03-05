---
title: Список Домаиннамереференцес
description: Получение списка directoryObject со ссылкой на домен. Возвращаемый список будет содержать все объекты каталога с зависимостью от домена.
author: davidmu1
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 132a0449e2c8b586f9d42f818dbfc90d6e25957a
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42433610"
---
# <a name="list-domainnamereferences"></a><span data-ttu-id="06319-104">Список Домаиннамереференцес</span><span class="sxs-lookup"><span data-stu-id="06319-104">List domainNameReferences</span></span>

<span data-ttu-id="06319-105">Пространство имен: Microsoft. Graph</span><span class="sxs-lookup"><span data-stu-id="06319-105">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="06319-106">Получение списка [directoryObject](../resources/directoryobject.md) со ссылкой на домен.</span><span class="sxs-lookup"><span data-stu-id="06319-106">Retrieve a list of [directoryObject](../resources/directoryobject.md) with a reference to the domain.</span></span> <span data-ttu-id="06319-107">Возвращаемый список будет содержать все объекты каталога с зависимостью от домена.</span><span class="sxs-lookup"><span data-stu-id="06319-107">The returned list will contain all directory objects that have a dependency on the domain.</span></span>

## <a name="permissions"></a><span data-ttu-id="06319-108">Разрешения</span><span class="sxs-lookup"><span data-stu-id="06319-108">Permissions</span></span>

<span data-ttu-id="06319-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="06319-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="06319-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="06319-111">Permission type</span></span>      | <span data-ttu-id="06319-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="06319-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="06319-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="06319-113">Delegated (work or school account)</span></span> | <span data-ttu-id="06319-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="06319-114">Not supported.</span></span> |
|<span data-ttu-id="06319-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="06319-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="06319-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="06319-116">Not supported.</span></span>    |
|<span data-ttu-id="06319-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="06319-117">Application</span></span> | <span data-ttu-id="06319-118">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="06319-118">Domain.ReadWrite.All</span></span> |

[!INCLUDE [limited-info](../../includes/limited-info.md)]

## <a name="http-request"></a><span data-ttu-id="06319-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="06319-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}/domainNameReferences
```

> <span data-ttu-id="06319-120">В качестве параметра {id} укажите домен, используя его полное доменное имя.</span><span class="sxs-lookup"><span data-stu-id="06319-120">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="06319-121">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="06319-121">Optional query parameters</span></span>

<span data-ttu-id="06319-122">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="06319-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="06319-123">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="06319-123">Request headers</span></span>

| <span data-ttu-id="06319-124">Имя</span><span class="sxs-lookup"><span data-stu-id="06319-124">Name</span></span>      |<span data-ttu-id="06319-125">Описание</span><span class="sxs-lookup"><span data-stu-id="06319-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="06319-126">Авторизация</span><span class="sxs-lookup"><span data-stu-id="06319-126">Authorization</span></span>  | <span data-ttu-id="06319-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="06319-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="06319-129">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="06319-129">Request body</span></span>

<span data-ttu-id="06319-130">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="06319-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="06319-131">Ответ</span><span class="sxs-lookup"><span data-stu-id="06319-131">Response</span></span>

<span data-ttu-id="06319-132">В случае успеха этот метод возвращает код отклика `200 OK` и коллекцию объектов [directoryObject](../resources/directoryobject.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="06319-132">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="06319-133">Пример</span><span class="sxs-lookup"><span data-stu-id="06319-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="06319-134">Запрос</span><span class="sxs-lookup"><span data-stu-id="06319-134">Request</span></span>


# <a name="http"></a>[<span data-ttu-id="06319-135">HTTP</span><span class="sxs-lookup"><span data-stu-id="06319-135">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_domainnamereferences"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/domains/contoso.com/domainNameReferences
```
# <a name="c"></a>[<span data-ttu-id="06319-136">C#</span><span class="sxs-lookup"><span data-stu-id="06319-136">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-domainnamereferences-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="06319-137">JavaScript</span><span class="sxs-lookup"><span data-stu-id="06319-137">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-domainnamereferences-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="06319-138">Objective-C</span><span class="sxs-lookup"><span data-stu-id="06319-138">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-domainnamereferences-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="06319-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="06319-139">Response</span></span>
<span data-ttu-id="06319-p105">Примечание. Представленный здесь объект отклика может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="06319-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
        "odata.type": "Microsoft.DirectoryServices.User",
        "objectType": "User",
        "objectId": "567a0db6-289c-43f7-a650-2645c03cbbbb",
        "accountEnabled": true,
        "displayName": "TestUser1",
        "facsimileTelephoneNumber": null,
        "mailNickname": "testuser1",
        "mobile": null,
        "userPrincipalName": "testuser1@contoso.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "List domainNameReferences",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
