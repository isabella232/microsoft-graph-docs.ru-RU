---
title: Вывод записи
description: 'Получение свойств и связей публикации в указанной цепочке. Вы можете указать и родительский элемент '
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: 755ec6156912d830bf6d13b95a599546ec53f411
ms.sourcegitcommit: b8d01acfc1cb7610a0e1f5c18065da415bae0777
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2019
ms.locfileid: "33608865"
---
# <a name="get-post"></a><span data-ttu-id="c1739-104">Вывод записи</span><span class="sxs-lookup"><span data-stu-id="c1739-104">Get post</span></span>

<span data-ttu-id="c1739-p102">Получение свойств и связей записи в указанной цепочке. Вы можете задать родительскую беседу вместе с цепочкой или только цепочку, не ссылаясь на родительскую беседу.</span><span class="sxs-lookup"><span data-stu-id="c1739-p102">Get the properties and relationships of a post in a specified thread. You can specify both the parent conversation and the thread, or, you can specify the thread without referencing the parent conversation.</span></span>

<span data-ttu-id="c1739-107">Так как ресурс **POST** поддерживает [расширения](/graph/extensibility-overview), с помощью `GET` операции можно также получить настраиваемые свойства и данные расширения в экземпляре **POST** .</span><span class="sxs-lookup"><span data-stu-id="c1739-107">Since the **post** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in a **post** instance.</span></span>

## <a name="permissions"></a><span data-ttu-id="c1739-108">Разрешения</span><span class="sxs-lookup"><span data-stu-id="c1739-108">Permissions</span></span>
<span data-ttu-id="c1739-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c1739-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c1739-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="c1739-111">Permission type</span></span>      | <span data-ttu-id="c1739-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="c1739-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c1739-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c1739-113">Delegated (work or school account)</span></span> | <span data-ttu-id="c1739-114">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c1739-114">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c1739-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="c1739-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c1739-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1739-116">Not supported.</span></span>    |
|<span data-ttu-id="c1739-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="c1739-117">Application</span></span> | <span data-ttu-id="c1739-118">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c1739-118">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c1739-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="c1739-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts/{id}
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c1739-120">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="c1739-120">Optional query parameters</span></span>
<span data-ttu-id="c1739-121">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="c1739-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c1739-122">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="c1739-122">Request headers</span></span>
| <span data-ttu-id="c1739-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c1739-123">Header</span></span>       | <span data-ttu-id="c1739-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c1739-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c1739-125">Авторизация</span><span class="sxs-lookup"><span data-stu-id="c1739-125">Authorization</span></span>  | <span data-ttu-id="c1739-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="c1739-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c1739-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="c1739-128">Request body</span></span>
<span data-ttu-id="c1739-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="c1739-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c1739-130">Ответ</span><span class="sxs-lookup"><span data-stu-id="c1739-130">Response</span></span>

<span data-ttu-id="c1739-131">В случае успеха этот метод возвращает код отклика `200 OK` и объект [post](../resources/post.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="c1739-131">If successful, this method returns a `200 OK` response code and [post](../resources/post.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c1739-132">Пример</span><span class="sxs-lookup"><span data-stu-id="c1739-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c1739-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="c1739-133">Request</span></span>
<span data-ttu-id="c1739-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="c1739-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_post"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}
```
##### <a name="response"></a><span data-ttu-id="c1739-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="c1739-135">Response</span></span>
<span data-ttu-id="c1739-p105">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="c1739-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.post"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 414

{
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "receivedDateTime": "datetime-value",
  "hasAttachments": true,
  "from": {
    "emailAddress": {
      "name": "name-value",
      "address": "address-value"
    }
  },
  "sender": {
    "emailAddress": {
      "name": "name-value",
      "address": "address-value"
    }
  }
}
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="c1739-139">Пример кода для SDK</span><span class="sxs-lookup"><span data-stu-id="c1739-139">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="c1739-140">Языках</span><span class="sxs-lookup"><span data-stu-id="c1739-140">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/get_post-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="c1739-141">Язык</span><span class="sxs-lookup"><span data-stu-id="c1739-141">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/get_post-Javascript-snippets.md)]

---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]

## <a name="see-also"></a><span data-ttu-id="c1739-142">См. также</span><span class="sxs-lookup"><span data-stu-id="c1739-142">See also</span></span>

- [<span data-ttu-id="c1739-143">Добавление пользовательских данных в ресурсы с помощью расширений</span><span class="sxs-lookup"><span data-stu-id="c1739-143">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="c1739-144">Добавление пользовательских данных в ресурсы user с помощью открытых расширений (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="c1739-144">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get post",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/v1.0/api/post-get.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/v1.0/api/post-get.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}-->
