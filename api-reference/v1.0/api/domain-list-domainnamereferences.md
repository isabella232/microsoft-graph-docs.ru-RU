---
title: Список Домаиннамереференцес
description: Получение списка directoryObject со ссылкой на домен. Возвращаемый список будет содержать все объекты каталога с зависимостью от домена.
author: davidmu1
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: dabfcedc940a86b1a7e6cb892cca8fee47e38fa0
ms.sourcegitcommit: bbef506636bce5b72351ee3834123771c301b1b1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "37726403"
---
# <a name="list-domainnamereferences"></a><span data-ttu-id="b8e14-104">Список Домаиннамереференцес</span><span class="sxs-lookup"><span data-stu-id="b8e14-104">List domainNameReferences</span></span>

<span data-ttu-id="b8e14-105">Получение списка [directoryObject](../resources/directoryobject.md) со ссылкой на домен.</span><span class="sxs-lookup"><span data-stu-id="b8e14-105">Retrieve a list of [directoryObject](../resources/directoryobject.md) with a reference to the domain.</span></span> <span data-ttu-id="b8e14-106">Возвращаемый список будет содержать все объекты каталога с зависимостью от домена.</span><span class="sxs-lookup"><span data-stu-id="b8e14-106">The returned list will contain all directory objects that have a dependency on the domain.</span></span>

## <a name="permissions"></a><span data-ttu-id="b8e14-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="b8e14-107">Permissions</span></span>

<span data-ttu-id="b8e14-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b8e14-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="b8e14-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="b8e14-110">Permission type</span></span>      | <span data-ttu-id="b8e14-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="b8e14-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b8e14-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b8e14-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b8e14-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b8e14-113">Not supported.</span></span> |
|<span data-ttu-id="b8e14-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="b8e14-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b8e14-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b8e14-115">Not supported.</span></span>    |
|<span data-ttu-id="b8e14-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="b8e14-116">Application</span></span> | <span data-ttu-id="b8e14-117">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b8e14-117">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b8e14-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="b8e14-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}/domainNameReferences
```

> <span data-ttu-id="b8e14-119">В качестве параметра {id} укажите домен, используя его полное доменное имя.</span><span class="sxs-lookup"><span data-stu-id="b8e14-119">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="b8e14-120">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="b8e14-120">Optional query parameters</span></span>

<span data-ttu-id="b8e14-121">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="b8e14-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b8e14-122">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="b8e14-122">Request headers</span></span>

| <span data-ttu-id="b8e14-123">Имя</span><span class="sxs-lookup"><span data-stu-id="b8e14-123">Name</span></span>      |<span data-ttu-id="b8e14-124">Описание</span><span class="sxs-lookup"><span data-stu-id="b8e14-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="b8e14-125">Авторизация</span><span class="sxs-lookup"><span data-stu-id="b8e14-125">Authorization</span></span>  | <span data-ttu-id="b8e14-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b8e14-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b8e14-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="b8e14-128">Request body</span></span>

<span data-ttu-id="b8e14-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="b8e14-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b8e14-130">Ответ</span><span class="sxs-lookup"><span data-stu-id="b8e14-130">Response</span></span>

<span data-ttu-id="b8e14-131">В случае успеха этот метод возвращает код отклика `200 OK` и коллекцию объектов [directoryObject](../resources/directoryobject.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="b8e14-131">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b8e14-132">Пример</span><span class="sxs-lookup"><span data-stu-id="b8e14-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b8e14-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="b8e14-133">Request</span></span>


# <a name="httptabhttp"></a>[<span data-ttu-id="b8e14-134">HTTP</span><span class="sxs-lookup"><span data-stu-id="b8e14-134">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_domainnamereferences"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/v1.0/domains/{domain-name}/domainNameReferences
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="b8e14-135">C#</span><span class="sxs-lookup"><span data-stu-id="b8e14-135">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-domainnamereferences-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="b8e14-136">JavaScript</span><span class="sxs-lookup"><span data-stu-id="b8e14-136">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-domainnamereferences-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="b8e14-137">Objective-C</span><span class="sxs-lookup"><span data-stu-id="b8e14-137">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-domainnamereferences-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="b8e14-138">Java</span><span class="sxs-lookup"><span data-stu-id="b8e14-138">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-domainnamereferences-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="b8e14-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="b8e14-139">Response</span></span>
<span data-ttu-id="b8e14-p105">Примечание. Представленный здесь объект отклика может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="b8e14-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
<!-- {
  "type": "#page.annotation",
  "description": "List domainNameReferences",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
