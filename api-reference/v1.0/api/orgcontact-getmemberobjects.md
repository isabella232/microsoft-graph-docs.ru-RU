---
title: 'orgContact: getMemberObjects'
description: Возврат всех групп, членом которых является это организационное Контактное лицо. Это транзитивная проверка.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: bbc577fe998d64a182051815124d364e9d3a7872
ms.sourcegitcommit: c9b9ff2c862f8d96d282a7bdf641cdb9c53a4600
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2019
ms.locfileid: "37633931"
---
# <a name="orgcontact-getmemberobjects"></a><span data-ttu-id="61e55-104">orgContact: getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="61e55-104">orgContact: getMemberObjects</span></span>

<span data-ttu-id="61e55-105">Возврат всех групп, членом которых является это [организационное Контактное лицо](../resources/orgcontact.md) .</span><span class="sxs-lookup"><span data-stu-id="61e55-105">Return all the groups that this [organizational contact](../resources/orgcontact.md) is a member of.</span></span> <span data-ttu-id="61e55-106">Это транзитивная проверка.</span><span class="sxs-lookup"><span data-stu-id="61e55-106">The check is transitive.</span></span> <span data-ttu-id="61e55-107">Организационные контакты не могут быть членами ролей каталогов.</span><span class="sxs-lookup"><span data-stu-id="61e55-107">Organizational contacts cannot be members of directory roles.</span></span> <span data-ttu-id="61e55-108">Роли каталога не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="61e55-108">No directory roles will be returned.</span></span>

## <a name="permissions"></a><span data-ttu-id="61e55-109">Разрешения</span><span class="sxs-lookup"><span data-stu-id="61e55-109">Permissions</span></span>
<span data-ttu-id="61e55-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="61e55-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="61e55-112">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="61e55-112">Permission type</span></span>      | <span data-ttu-id="61e55-113">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="61e55-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="61e55-114">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="61e55-114">Delegated (work or school account)</span></span> | <span data-ttu-id="61e55-115">OrgContact. Read. ALL и Group. Read. ALL, Directory. Read. ALL</span><span class="sxs-lookup"><span data-stu-id="61e55-115">OrgContact.Read.All and Group.Read.All, Directory.Read.All</span></span>  |
|<span data-ttu-id="61e55-116">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="61e55-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="61e55-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="61e55-117">Not supported.</span></span>    |
|<span data-ttu-id="61e55-118">Для приложения</span><span class="sxs-lookup"><span data-stu-id="61e55-118">Application</span></span> | <span data-ttu-id="61e55-119">OrgContact. Read. ALL и Group. Read. ALL, Directory. Read. ALL</span><span class="sxs-lookup"><span data-stu-id="61e55-119">OrgContact.Read.All and Group.Read.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="61e55-120">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="61e55-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /contacts/{id}/getMemberObjects

```
## <a name="request-headers"></a><span data-ttu-id="61e55-121">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="61e55-121">Request headers</span></span>
| <span data-ttu-id="61e55-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="61e55-122">Header</span></span>       | <span data-ttu-id="61e55-123">Значение</span><span class="sxs-lookup"><span data-stu-id="61e55-123">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="61e55-124">Авторизация</span><span class="sxs-lookup"><span data-stu-id="61e55-124">Authorization</span></span>  | <span data-ttu-id="61e55-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="61e55-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="61e55-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="61e55-127">Content-type</span></span>   | <span data-ttu-id="61e55-p105">application/json. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="61e55-p105">application/json. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="61e55-130">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="61e55-130">Request body</span></span>
<span data-ttu-id="61e55-131">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="61e55-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="61e55-132">Параметр</span><span class="sxs-lookup"><span data-stu-id="61e55-132">Parameter</span></span>    | <span data-ttu-id="61e55-133">Тип</span><span class="sxs-lookup"><span data-stu-id="61e55-133">Type</span></span>   |<span data-ttu-id="61e55-134">Описание</span><span class="sxs-lookup"><span data-stu-id="61e55-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="61e55-135">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="61e55-135">securityEnabledOnly</span></span>|<span data-ttu-id="61e55-136">Логическое</span><span class="sxs-lookup"><span data-stu-id="61e55-136">Boolean</span></span>|<span data-ttu-id="61e55-137">Значение `false`.</span><span class="sxs-lookup"><span data-stu-id="61e55-137">Set to `false`.</span></span> <span data-ttu-id="61e55-138">Возвращение лишь защищенных групп поддерживается только для пользователей.</span><span class="sxs-lookup"><span data-stu-id="61e55-138">Returning only security-enabled groups is supported for users only.</span></span>|

## <a name="response"></a><span data-ttu-id="61e55-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="61e55-139">Response</span></span>

<span data-ttu-id="61e55-140">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и объект коллекции String в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="61e55-140">If successful, this method returns a `200 OK` response code and a String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="61e55-141">Пример</span><span class="sxs-lookup"><span data-stu-id="61e55-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="61e55-142">Запрос</span><span class="sxs-lookup"><span data-stu-id="61e55-142">Request</span></span>
<span data-ttu-id="61e55-143">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="61e55-143">The following is an example of the request.</span></span>


# <a name="httptabhttp"></a>[<span data-ttu-id="61e55-144">HTTP</span><span class="sxs-lookup"><span data-stu-id="61e55-144">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "orgcontact_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/v1.0/contacts/{id}/getMemberObjects
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": false
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="61e55-145">C#</span><span class="sxs-lookup"><span data-stu-id="61e55-145">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/orgcontact-getmemberobjects-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="61e55-146">JavaScript</span><span class="sxs-lookup"><span data-stu-id="61e55-146">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/orgcontact-getmemberobjects-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="61e55-147">Objective-C</span><span class="sxs-lookup"><span data-stu-id="61e55-147">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/orgcontact-getmemberobjects-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="61e55-148">Java</span><span class="sxs-lookup"><span data-stu-id="61e55-148">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/orgcontact-getmemberobjects-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="61e55-149">Отклик</span><span class="sxs-lookup"><span data-stu-id="61e55-149">Response</span></span>
<span data-ttu-id="61e55-150">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="61e55-150">The following is an example of the response.</span></span>
><span data-ttu-id="61e55-151">**Примечание**. Объект отклика, показанный здесь, может быть сокращен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="61e55-151">**Note**: The response object shown here might be shortened for readability.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "value": [
    "groupID-value1"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "orgContact: getMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->