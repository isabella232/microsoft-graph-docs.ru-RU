---
title: Список Оргконтактс
description: Получение списка контактов Организации для этой Организации.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 36d4f5de0d4155afc0155e3eb7b713bdda66bc74
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35877855"
---
# <a name="list-orgcontacts"></a><span data-ttu-id="ea936-103">Список Оргконтактс</span><span class="sxs-lookup"><span data-stu-id="ea936-103">List orgContacts</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="ea936-104">Получение списка контактов Организации для этой Организации.</span><span class="sxs-lookup"><span data-stu-id="ea936-104">Retrieve the list of organizational contacts for this organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="ea936-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="ea936-105">Permissions</span></span>
<span data-ttu-id="ea936-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea936-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ea936-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="ea936-108">Permission type</span></span>      | <span data-ttu-id="ea936-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="ea936-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ea936-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="ea936-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ea936-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ea936-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="ea936-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="ea936-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ea936-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ea936-113">Not supported.</span></span>    |
|<span data-ttu-id="ea936-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="ea936-114">Application</span></span> | <span data-ttu-id="ea936-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea936-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ea936-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="ea936-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ea936-117">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="ea936-117">Optional query parameters</span></span>
<span data-ttu-id="ea936-118">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="ea936-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ea936-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="ea936-119">Request headers</span></span>
| <span data-ttu-id="ea936-120">Имя</span><span class="sxs-lookup"><span data-stu-id="ea936-120">Name</span></span>       | <span data-ttu-id="ea936-121">Тип</span><span class="sxs-lookup"><span data-stu-id="ea936-121">Type</span></span> | <span data-ttu-id="ea936-122">Описание</span><span class="sxs-lookup"><span data-stu-id="ea936-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ea936-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea936-123">Authorization</span></span>  | <span data-ttu-id="ea936-124">string</span><span class="sxs-lookup"><span data-stu-id="ea936-124">string</span></span>  | <span data-ttu-id="ea936-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ea936-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ea936-127">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="ea936-127">Request body</span></span>
<span data-ttu-id="ea936-128">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="ea936-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ea936-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="ea936-129">Response</span></span>

<span data-ttu-id="ea936-130">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и коллекцию объектов [orgContact](../resources/orgcontact.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="ea936-130">If successful, this method returns a `200 OK` response code and a collection of [orgContact](../resources/orgcontact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ea936-131">Пример</span><span class="sxs-lookup"><span data-stu-id="ea936-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ea936-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="ea936-132">Request</span></span>
<span data-ttu-id="ea936-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="ea936-133">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="ea936-134">HTTP</span><span class="sxs-lookup"><span data-stu-id="ea936-134">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "list_orgcontact"
}-->
```http
GET https://graph.microsoft.com/beta/contacts
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="ea936-135">C#</span><span class="sxs-lookup"><span data-stu-id="ea936-135">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/list-orgcontact-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="ea936-136">Javascript</span><span class="sxs-lookup"><span data-stu-id="ea936-136">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/list-orgcontact-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="ea936-137">Цель — C</span><span class="sxs-lookup"><span data-stu-id="ea936-137">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/list-orgcontact-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="ea936-138">Java</span><span class="sxs-lookup"><span data-stu-id="ea936-138">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/list-orgcontact-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="ea936-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="ea936-139">Response</span></span>
<span data-ttu-id="ea936-p103">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="ea936-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.orgcontact",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 222

{
  "value": [
    {
      "addresses":[
          {
            "city": "string",
            "countryOrRegion": "string",
            "officeLocation": "string",
            "postalCode": "string",
            "state": "string",
            "street": "string"
          }
      ],
      "companyName": "companyName-value",
      "department": "department-value",
      "displayName": "displayName-value",
      "phones":[
          {
            "type": "string",
            "number": "string"
          }
      ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "List orgContact",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
