---
title: Получение руководителя
description: Получение руководителя пользователя. Возвращает пользователя или контакт, назначенный в качестве руководителя пользователя.
localization_priority: Priority
author: dkershaw10
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 1f73127c95981bc22d4269e7a8e57aa570e64f2b
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42509075"
---
# <a name="list-manager"></a><span data-ttu-id="c3d4f-104">Получение руководителя</span><span class="sxs-lookup"><span data-stu-id="c3d4f-104">List manager</span></span>

<span data-ttu-id="c3d4f-105">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="c3d4f-105">Namespace: microsoft.graph</span></span>

<span data-ttu-id="c3d4f-106">Получение руководителя пользователя.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-106">Get user's manager.</span></span> <span data-ttu-id="c3d4f-107">Возвращает пользователя или контакт организации, назначенный в качестве руководителя пользователя.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-107">Returns the user or organizational contact assigned as the user's manager.</span></span>
## <a name="permissions"></a><span data-ttu-id="c3d4f-108">Разрешения</span><span class="sxs-lookup"><span data-stu-id="c3d4f-108">Permissions</span></span>
<span data-ttu-id="c3d4f-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c3d4f-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c3d4f-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="c3d4f-111">Permission type</span></span>      | <span data-ttu-id="c3d4f-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="c3d4f-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c3d4f-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c3d4f-113">Delegated (work or school account)</span></span> | <span data-ttu-id="c3d4f-114">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c3d4f-114">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c3d4f-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="c3d4f-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c3d4f-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-116">Not supported.</span></span>    |
|<span data-ttu-id="c3d4f-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="c3d4f-117">Application</span></span> | <span data-ttu-id="c3d4f-118">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3d4f-118">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

[!INCLUDE [limited-info](../../includes/limited-info.md)]

## <a name="http-request"></a><span data-ttu-id="c3d4f-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="c3d4f-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/manager
GET /users/{id | userPrincipalName}/manager
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c3d4f-120">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="c3d4f-120">Optional query parameters</span></span>
<span data-ttu-id="c3d4f-121">Этот метод поддерживает [параметры запросов OData](/graph/query-parameters) для настройки отклика.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-121">This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c3d4f-122">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="c3d4f-122">Request headers</span></span>
| <span data-ttu-id="c3d4f-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c3d4f-123">Header</span></span>       | <span data-ttu-id="c3d4f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c3d4f-124">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="c3d4f-125">Авторизация</span><span class="sxs-lookup"><span data-stu-id="c3d4f-125">Authorization</span></span>  | <span data-ttu-id="c3d4f-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c3d4f-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="c3d4f-128">Request body</span></span>
<span data-ttu-id="c3d4f-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c3d4f-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="c3d4f-130">Response</span></span>

<span data-ttu-id="c3d4f-131">В случае успеха этот метод возвращает код отклика `200 OK` и объект [directoryObject](../resources/directoryobject.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-131">If successful, this method returns a `200 OK` response code and a [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c3d4f-132">Пример</span><span class="sxs-lookup"><span data-stu-id="c3d4f-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c3d4f-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="c3d4f-133">Request</span></span>
<span data-ttu-id="c3d4f-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-134">The following is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="c3d4f-135">HTTP</span><span class="sxs-lookup"><span data-stu-id="c3d4f-135">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_manager"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/manager
```
# <a name="c"></a>[<span data-ttu-id="c3d4f-136">C#</span><span class="sxs-lookup"><span data-stu-id="c3d4f-136">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-manager-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="c3d4f-137">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c3d4f-137">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-manager-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="c3d4f-138">Objective-C</span><span class="sxs-lookup"><span data-stu-id="c3d4f-138">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-manager-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="c3d4f-139">Java</span><span class="sxs-lookup"><span data-stu-id="c3d4f-139">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-manager-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="c3d4f-140">Отклик</span><span class="sxs-lookup"><span data-stu-id="c3d4f-140">Response</span></span>
<span data-ttu-id="c3d4f-141">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-141">The following is an example of the response.</span></span>
><span data-ttu-id="c3d4f-142">**Примечание**. Объект отклика, показанный здесь, может быть сокращен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-142">**Note**: The response object shown here might be shortened for readability.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "objectType": "User",
  "id": "111048d2-2761-4347-b978-07354283363b",
  "accountEnabled": true,
  "city": "San Diego",
  "country": "United States",
  "department": "Sales & Marketing",
  "displayName": "Sara Davis",
  "givenName": "Sara",
  "jobTitle": "Finance VP",
  "mail": "SaraD@contoso.onmicrosoft.com",
  "mailNickname": "SaraD",
  "state": "CA",
  "streetAddress": "9256 Towne Center Dr., Suite 400",
  "surname": "Davis",
  "usageLocation": "US",
  "userPrincipalName": "SaraD@contoso.onmicrosoft.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directReports",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
