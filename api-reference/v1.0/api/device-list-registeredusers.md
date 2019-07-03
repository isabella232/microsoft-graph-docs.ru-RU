---
title: Список registeredUsers
description: Получение списка пользователей, являющихся зарегистрированными пользователями устройства.
author: davidmu1
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: d7901498156fddf7eb228a0d5eb957d4f615a824
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35459471"
---
# <a name="list-registeredusers"></a><span data-ttu-id="96892-103">Список registeredUsers</span><span class="sxs-lookup"><span data-stu-id="96892-103">List registeredUsers</span></span>

<span data-ttu-id="96892-104">Получение списка пользователей, являющихся зарегистрированными пользователями устройства.</span><span class="sxs-lookup"><span data-stu-id="96892-104">Retrieve a list of users that are registered users of the device.</span></span>

<span data-ttu-id="96892-105">В случае зарегистрированных личных устройств или устройств, присоединенных через облако, при регистрации для обычных пользователей задается то же значение, что и для владельцев.</span><span class="sxs-lookup"><span data-stu-id="96892-105">For cloud joined devices and registered personal devices, registered users are set to the same value as registered owners at the time of registration.</span></span>

## <a name="permissions"></a><span data-ttu-id="96892-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="96892-106">Permissions</span></span>
<span data-ttu-id="96892-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="96892-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="96892-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="96892-109">Permission type</span></span>      | <span data-ttu-id="96892-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="96892-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="96892-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="96892-111">Delegated (work or school account)</span></span> | <span data-ttu-id="96892-112">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="96892-112">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="96892-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="96892-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="96892-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="96892-114">Not supported.</span></span>    |
|<span data-ttu-id="96892-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="96892-115">Application</span></span> | <span data-ttu-id="96892-116">Directory.Read.All или Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="96892-116">Directory.Read.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="96892-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="96892-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}/registeredUsers
```
## <a name="optional-query-parameters"></a><span data-ttu-id="96892-118">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="96892-118">Optional query parameters</span></span>
<span data-ttu-id="96892-119">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="96892-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="96892-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="96892-120">Request headers</span></span>
| <span data-ttu-id="96892-121">Имя</span><span class="sxs-lookup"><span data-stu-id="96892-121">Name</span></span>       | <span data-ttu-id="96892-122">Тип</span><span class="sxs-lookup"><span data-stu-id="96892-122">Type</span></span> | <span data-ttu-id="96892-123">Описание</span><span class="sxs-lookup"><span data-stu-id="96892-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="96892-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="96892-124">Authorization</span></span>  | <span data-ttu-id="96892-125">string</span><span class="sxs-lookup"><span data-stu-id="96892-125">string</span></span>  | <span data-ttu-id="96892-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="96892-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="96892-128">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="96892-128">Request body</span></span>
<span data-ttu-id="96892-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="96892-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="96892-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="96892-130">Response</span></span>

<span data-ttu-id="96892-131">В случае успеха этот метод возвращает код отклика `200 OK` и коллекцию объектов [directoryObject](../resources/directoryobject.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="96892-131">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="96892-132">Пример</span><span class="sxs-lookup"><span data-stu-id="96892-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="96892-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="96892-133">Request</span></span>
<span data-ttu-id="96892-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="96892-134">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="96892-135">HTTP</span><span class="sxs-lookup"><span data-stu-id="96892-135">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_registeredusers"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}/registeredUsers
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="96892-136">C#</span><span class="sxs-lookup"><span data-stu-id="96892-136">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-registeredusers-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="96892-137">Javascript</span><span class="sxs-lookup"><span data-stu-id="96892-137">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-registeredusers-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="96892-138">Цель — C</span><span class="sxs-lookup"><span data-stu-id="96892-138">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-registeredusers-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="96892-139">Ответ</span><span class="sxs-lookup"><span data-stu-id="96892-139">Response</span></span>
<span data-ttu-id="96892-p103">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="96892-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List registeredUsers",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
