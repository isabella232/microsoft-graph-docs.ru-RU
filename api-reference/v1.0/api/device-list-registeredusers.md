---
title: Список registeredUsers
description: Получение списка пользователей, являющихся зарегистрированными пользователями устройства.
author: davidmu1
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 6c03db1f6b2b00a587ea2b6d5935aa740196c360
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40864854"
---
# <a name="list-registeredusers"></a><span data-ttu-id="6a41b-103">Список registeredUsers</span><span class="sxs-lookup"><span data-stu-id="6a41b-103">List registeredUsers</span></span>

<span data-ttu-id="6a41b-104">Получение списка пользователей, являющихся зарегистрированными пользователями устройства.</span><span class="sxs-lookup"><span data-stu-id="6a41b-104">Retrieve a list of users that are registered users of the device.</span></span>

<span data-ttu-id="6a41b-105">В случае зарегистрированных личных устройств или устройств, присоединенных через облако, при регистрации для обычных пользователей задается то же значение, что и для владельцев.</span><span class="sxs-lookup"><span data-stu-id="6a41b-105">For cloud joined devices and registered personal devices, registered users are set to the same value as registered owners at the time of registration.</span></span>

## <a name="permissions"></a><span data-ttu-id="6a41b-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="6a41b-106">Permissions</span></span>
<span data-ttu-id="6a41b-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6a41b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6a41b-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="6a41b-109">Permission type</span></span>      | <span data-ttu-id="6a41b-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="6a41b-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6a41b-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6a41b-111">Delegated (work or school account)</span></span> | <span data-ttu-id="6a41b-112">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6a41b-112">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="6a41b-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="6a41b-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6a41b-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6a41b-114">Not supported.</span></span>    |
|<span data-ttu-id="6a41b-115">Приложение</span><span class="sxs-lookup"><span data-stu-id="6a41b-115">Application</span></span> | <span data-ttu-id="6a41b-116">Directory.Read.All или Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6a41b-116">Directory.Read.All or Directory.ReadWrite.All</span></span> |

[!INCLUDE [limited-info](../../includes/limited-info.md)]

## <a name="http-request"></a><span data-ttu-id="6a41b-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="6a41b-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}/registeredUsers
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6a41b-118">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="6a41b-118">Optional query parameters</span></span>
<span data-ttu-id="6a41b-119">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="6a41b-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="6a41b-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="6a41b-120">Request headers</span></span>
| <span data-ttu-id="6a41b-121">Имя</span><span class="sxs-lookup"><span data-stu-id="6a41b-121">Name</span></span>       | <span data-ttu-id="6a41b-122">Тип</span><span class="sxs-lookup"><span data-stu-id="6a41b-122">Type</span></span> | <span data-ttu-id="6a41b-123">Описание</span><span class="sxs-lookup"><span data-stu-id="6a41b-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6a41b-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="6a41b-124">Authorization</span></span>  | <span data-ttu-id="6a41b-125">string</span><span class="sxs-lookup"><span data-stu-id="6a41b-125">string</span></span>  | <span data-ttu-id="6a41b-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6a41b-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6a41b-128">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="6a41b-128">Request body</span></span>
<span data-ttu-id="6a41b-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="6a41b-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6a41b-130">Ответ</span><span class="sxs-lookup"><span data-stu-id="6a41b-130">Response</span></span>

<span data-ttu-id="6a41b-131">В случае успеха этот метод возвращает код отклика `200 OK` и коллекцию объектов [directoryObject](../resources/directoryobject.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="6a41b-131">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6a41b-132">Пример</span><span class="sxs-lookup"><span data-stu-id="6a41b-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6a41b-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="6a41b-133">Request</span></span>
<span data-ttu-id="6a41b-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="6a41b-134">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="6a41b-135">HTTP</span><span class="sxs-lookup"><span data-stu-id="6a41b-135">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_registeredusers"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/v1.0/devices/{id}/registeredUsers
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="6a41b-136">C#</span><span class="sxs-lookup"><span data-stu-id="6a41b-136">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-registeredusers-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="6a41b-137">JavaScript</span><span class="sxs-lookup"><span data-stu-id="6a41b-137">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-registeredusers-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="6a41b-138">Objective-C</span><span class="sxs-lookup"><span data-stu-id="6a41b-138">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-registeredusers-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="6a41b-139">Java</span><span class="sxs-lookup"><span data-stu-id="6a41b-139">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-registeredusers-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="6a41b-140">Ответ</span><span class="sxs-lookup"><span data-stu-id="6a41b-140">Response</span></span>
<span data-ttu-id="6a41b-p103">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="6a41b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
