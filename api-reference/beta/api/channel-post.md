---
title: Создание канала
description: Создание канала в Microsoft Team, как указано в тексте запроса.
localization_priority: Normal
author: nkramer
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: 252f46a399d3e0665461f2f55e22467a07bf0e4e
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "36317443"
---
# <a name="create-channel"></a><span data-ttu-id="05fa2-103">Создание канала</span><span class="sxs-lookup"><span data-stu-id="05fa2-103">Create Channel</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="05fa2-104">Создание [канала](../resources/channel.md) в Microsoft Team, как указано в тексте запроса.</span><span class="sxs-lookup"><span data-stu-id="05fa2-104">Create a new [channel](../resources/channel.md) in a Microsoft Team, as specified in the request body.</span></span>

> <span data-ttu-id="05fa2-105">**Примечание**. Существует известная проблема с разрешениями для приложений и этим API.</span><span class="sxs-lookup"><span data-stu-id="05fa2-105">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="05fa2-106">Дополнительные сведения см. в [списке известных проблем](/graph/known-issues#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="05fa2-106">For details, see the [known issues list](/graph/known-issues#application-permissions).</span></span>

## <a name="permissions"></a><span data-ttu-id="05fa2-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="05fa2-107">Permissions</span></span>
<span data-ttu-id="05fa2-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="05fa2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="05fa2-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="05fa2-110">Permission type</span></span>      | <span data-ttu-id="05fa2-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="05fa2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="05fa2-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="05fa2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="05fa2-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="05fa2-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="05fa2-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="05fa2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="05fa2-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="05fa2-115">Not supported.</span></span>    |
|<span data-ttu-id="05fa2-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="05fa2-116">Application</span></span> | <span data-ttu-id="05fa2-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="05fa2-117">Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="05fa2-118">**Примечание**. Этот API поддерживает разрешения администратора.</span><span class="sxs-lookup"><span data-stu-id="05fa2-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="05fa2-119">Глобальные администраторы и администраторы службы Microsoft Teams могут получать доступ к командам, в которых они не состоят.</span><span class="sxs-lookup"><span data-stu-id="05fa2-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="05fa2-120">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="05fa2-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/channels
```
## <a name="request-headers"></a><span data-ttu-id="05fa2-121">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="05fa2-121">Request headers</span></span>
| <span data-ttu-id="05fa2-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="05fa2-122">Header</span></span>       | <span data-ttu-id="05fa2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="05fa2-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="05fa2-124">Авторизация</span><span class="sxs-lookup"><span data-stu-id="05fa2-124">Authorization</span></span>  | <span data-ttu-id="05fa2-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="05fa2-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="05fa2-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="05fa2-127">Content-Type</span></span>  | <span data-ttu-id="05fa2-128">application/json</span><span class="sxs-lookup"><span data-stu-id="05fa2-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="05fa2-129">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="05fa2-129">Request body</span></span>
<span data-ttu-id="05fa2-130">Предоставьте в тексте запроса описание объекта [channel](../resources/channel.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="05fa2-130">In the request body, supply a JSON representation of [channel](../resources/channel.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="05fa2-131">Отклик</span><span class="sxs-lookup"><span data-stu-id="05fa2-131">Response</span></span>

<span data-ttu-id="05fa2-132">В случае успеха этот метод возвращает код отклика `201 Created` и объект [channel](../resources/channel.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="05fa2-132">If successful, this method returns `201 Created` response code and [channel](../resources/channel.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="05fa2-133">Пример</span><span class="sxs-lookup"><span data-stu-id="05fa2-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="05fa2-134">Запрос</span><span class="sxs-lookup"><span data-stu-id="05fa2-134">Request</span></span>
<span data-ttu-id="05fa2-135">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="05fa2-135">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="05fa2-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="05fa2-136">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_channel_from_group"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/channels
Content-type: application/json

{
  "displayName": "Architecture Discussion",
  "description": "This channel is where we debate all future architecture plans"
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="05fa2-137">C#</span><span class="sxs-lookup"><span data-stu-id="05fa2-137">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-channel-from-group-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="05fa2-138">JavaScript</span><span class="sxs-lookup"><span data-stu-id="05fa2-138">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-channel-from-group-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="05fa2-139">Цель — C</span><span class="sxs-lookup"><span data-stu-id="05fa2-139">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-channel-from-group-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="05fa2-140">Java</span><span class="sxs-lookup"><span data-stu-id="05fa2-140">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/create-channel-from-group-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="05fa2-141">Отклик</span><span class="sxs-lookup"><span data-stu-id="05fa2-141">Response</span></span>
<span data-ttu-id="05fa2-p105">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="05fa2-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.channel"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
  "id": "id-value",
  "displayName": "Architecture Discussion",
  "description": "This channel is where we debate all future architecture plans"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create Channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
