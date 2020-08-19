---
title: Список переопределений
description: Получение переопределений, настроенных пользователем для классификации сообщений от определенных отправителей.
localization_priority: Normal
author: svpsiva
ms.prod: ''
doc_type: apiPageType
ms.openlocfilehash: a0a54566f2fd51c226e849be108125fd358edc08
ms.sourcegitcommit: a6d284b3726139f11194aa3d23b8bb79165cc09e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "46806179"
---
# <a name="list-overrides"></a><span data-ttu-id="b489c-103">Список переопределений</span><span class="sxs-lookup"><span data-stu-id="b489c-103">List overrides</span></span>

<span data-ttu-id="b489c-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="b489c-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="b489c-105">Получение переопределений, настроенных пользователем для классификации сообщений от определенных отправителей.</span><span class="sxs-lookup"><span data-stu-id="b489c-105">Get the overrides that a user has set up to always classify messages from certain senders in specific ways.</span></span>

<span data-ttu-id="b489c-p101">Каждое переопределение соответствует SMTP-адресу отправителя. Изначально у пользователя нет переопределений.</span><span class="sxs-lookup"><span data-stu-id="b489c-p101">Each override corresponds to an SMTP address of a sender. Initially, a user does not have any overrides.</span></span>
## <a name="permissions"></a><span data-ttu-id="b489c-108">Разрешения</span><span class="sxs-lookup"><span data-stu-id="b489c-108">Permissions</span></span>
<span data-ttu-id="b489c-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b489c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b489c-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="b489c-111">Permission type</span></span>      | <span data-ttu-id="b489c-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="b489c-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b489c-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b489c-113">Delegated (work or school account)</span></span> | <span data-ttu-id="b489c-114">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="b489c-114">Mail.Read</span></span>    |
|<span data-ttu-id="b489c-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="b489c-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b489c-116">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="b489c-116">Mail.Read</span></span>    |
|<span data-ttu-id="b489c-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="b489c-117">Application</span></span> | <span data-ttu-id="b489c-118">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="b489c-118">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="b489c-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="b489c-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/inferenceClassification/overrides
GET /users/{id}/inferenceClassification/overrides
```

## <a name="request-headers"></a><span data-ttu-id="b489c-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="b489c-120">Request headers</span></span>
| <span data-ttu-id="b489c-121">Имя</span><span class="sxs-lookup"><span data-stu-id="b489c-121">Name</span></span>       | <span data-ttu-id="b489c-122">Тип</span><span class="sxs-lookup"><span data-stu-id="b489c-122">Type</span></span> | <span data-ttu-id="b489c-123">Описание</span><span class="sxs-lookup"><span data-stu-id="b489c-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b489c-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="b489c-124">Authorization</span></span>  | <span data-ttu-id="b489c-125">string</span><span class="sxs-lookup"><span data-stu-id="b489c-125">string</span></span>  | <span data-ttu-id="b489c-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b489c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b489c-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="b489c-128">Request body</span></span>
<span data-ttu-id="b489c-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="b489c-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b489c-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="b489c-130">Response</span></span>

<span data-ttu-id="b489c-p104">В случае успешного выполнения этот метод возвращает код отклика `200 OK` и коллекцию объектов [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) в тексте отклика. Если у пользователя нет настроенных переопределений, возвращается пустая коллекция.</span><span class="sxs-lookup"><span data-stu-id="b489c-p104">If successful, this method returns a `200 OK` response code and a collection of [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) objects in the response body. An empty collection is returned if the user doesn't have any overrides set up.</span></span>
## <a name="example"></a><span data-ttu-id="b489c-133">Пример</span><span class="sxs-lookup"><span data-stu-id="b489c-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b489c-134">Запрос</span><span class="sxs-lookup"><span data-stu-id="b489c-134">Request</span></span>
<span data-ttu-id="b489c-135">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="b489c-135">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="b489c-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="b489c-136">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_overrides"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides
```
# <a name="c"></a>[<span data-ttu-id="b489c-137">C#</span><span class="sxs-lookup"><span data-stu-id="b489c-137">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-overrides-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="b489c-138">JavaScript</span><span class="sxs-lookup"><span data-stu-id="b489c-138">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-overrides-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="b489c-139">Objective-C</span><span class="sxs-lookup"><span data-stu-id="b489c-139">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-overrides-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="b489c-140">Java</span><span class="sxs-lookup"><span data-stu-id="b489c-140">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-overrides-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="b489c-141">Отклик</span><span class="sxs-lookup"><span data-stu-id="b489c-141">Response</span></span>
<span data-ttu-id="b489c-p105">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="b489c-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.inferenceClassificationOverride",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "classifyAs": "focused",
      "senderEmailAddress": {
        "name": "Samantha Booth",
        "address": "samanthab@adatum.onmicrosoft.com"
      },
      "id": "98f5bdef-576a-404d-a2ea-07a3cf11a9b9"
    },
    {
      "classifyAs": "other",
      "senderEmailAddress": {
        "name": "Randi Welch",
        "address": "randiw@adatum.onmicrosoft.com"
      },
      "id": "98f5bdef-576a-404d-a2ea-07a3cf34af4r"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List overrides",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
