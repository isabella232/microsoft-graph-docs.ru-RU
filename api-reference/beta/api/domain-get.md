---
title: Получение домена
description: Получение свойств и связей объекта домена.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: f69d9d17445d7b7570f655a610aee5fe30c15aa7
ms.sourcegitcommit: b8d01acfc1cb7610a0e1f5c18065da415bae0777
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2019
ms.locfileid: "33589326"
---
# <a name="get-domain"></a><span data-ttu-id="41517-103">Получение домена</span><span class="sxs-lookup"><span data-stu-id="41517-103">Get domain</span></span>

<span data-ttu-id="41517-104">Получение свойств и связей объекта домена.</span><span class="sxs-lookup"><span data-stu-id="41517-104">Retrieve the properties and relationships of domain object.</span></span>

## <a name="permissions"></a><span data-ttu-id="41517-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="41517-105">Permissions</span></span>

<span data-ttu-id="41517-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="41517-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="41517-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="41517-108">Permission type</span></span>      | <span data-ttu-id="41517-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="41517-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="41517-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="41517-110">Delegated (work or school account)</span></span> | <span data-ttu-id="41517-111">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="41517-111">Directory.Read.All</span></span>    |
|<span data-ttu-id="41517-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="41517-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="41517-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41517-113">Not supported.</span></span>    |
|<span data-ttu-id="41517-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="41517-114">Application</span></span> | <span data-ttu-id="41517-115">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="41517-115">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="41517-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="41517-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}
```

> <span data-ttu-id="41517-117">В качестве параметра {id} укажите домен, используя его полное доменное имя.</span><span class="sxs-lookup"><span data-stu-id="41517-117">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="41517-118">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="41517-118">Optional query parameters</span></span>

<span data-ttu-id="41517-119">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="41517-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="41517-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="41517-120">Request headers</span></span>

| <span data-ttu-id="41517-121">Имя</span><span class="sxs-lookup"><span data-stu-id="41517-121">Name</span></span>      |<span data-ttu-id="41517-122">Описание</span><span class="sxs-lookup"><span data-stu-id="41517-122">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="41517-123">Авторизация</span><span class="sxs-lookup"><span data-stu-id="41517-123">Authorization</span></span>  | <span data-ttu-id="41517-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="41517-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="41517-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="41517-126">Content-Type</span></span>  | <span data-ttu-id="41517-127">application/json</span><span class="sxs-lookup"><span data-stu-id="41517-127">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="41517-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="41517-128">Request body</span></span>
<span data-ttu-id="41517-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="41517-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="41517-130">Ответ</span><span class="sxs-lookup"><span data-stu-id="41517-130">Response</span></span>

<span data-ttu-id="41517-131">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и объект [domain](../resources/domain.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="41517-131">If successful, this method returns a `200 OK` response code and [domain](../resources/domain.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="41517-132">Пример</span><span class="sxs-lookup"><span data-stu-id="41517-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="41517-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="41517-133">Request</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["contoso.com"],
  "name": "get_domain"
}-->
```http
GET https://graph.microsoft.com/v1.0/domains/contoso.com
```
##### <a name="response"></a><span data-ttu-id="41517-134">Отклик</span><span class="sxs-lookup"><span data-stu-id="41517-134">Response</span></span>
<span data-ttu-id="41517-p103">Примечание. Представленный здесь объект отклика может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="41517-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domain"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 192

{
  "authenticationType": "authenticationType-value",
  "availabilityStatus": "availabilityStatus-value",
  "id": "contoso.com",
  "isAdminManaged": true,
  "isDefault": true,
  "isInitial": true,
  "isRoot": true
}
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="41517-137">Пример кода для SDK</span><span class="sxs-lookup"><span data-stu-id="41517-137">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="41517-138">Языках</span><span class="sxs-lookup"><span data-stu-id="41517-138">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/get_domain-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="41517-139">Язык</span><span class="sxs-lookup"><span data-stu-id="41517-139">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/get_domain-Javascript-snippets.md)]

---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get domain",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/v1.0/api/domain-get.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/v1.0/api/domain-get.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}-->
