---
title: Обновление объекта conversationThread
description: Блокировка и разблокировка, позволяющие разрешить или предотвратить дальнейшую публикацию записей в цепочке.
ms.openlocfilehash: 0d9de78717aeb35afa5b114f07430d9fc3e5e8fe
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27079364"
---
# <a name="update-conversationthread"></a><span data-ttu-id="c13c7-103">Обновление объекта conversationThread</span><span class="sxs-lookup"><span data-stu-id="c13c7-103">Update conversationthread</span></span>

> <span data-ttu-id="c13c7-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="c13c7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c13c7-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c13c7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c13c7-106">Блокировка и разблокировка, позволяющие разрешить или предотвратить дальнейшую публикацию записей в цепочке.</span><span class="sxs-lookup"><span data-stu-id="c13c7-106">Lock or unlock a thread, to allow or avoid further posting to the thread.</span></span>
## <a name="permissions"></a><span data-ttu-id="c13c7-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="c13c7-107">Permissions</span></span>
<span data-ttu-id="c13c7-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c13c7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c13c7-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="c13c7-110">Permission type</span></span>      | <span data-ttu-id="c13c7-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="c13c7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c13c7-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c13c7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c13c7-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c13c7-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c13c7-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="c13c7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c13c7-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c13c7-115">Not supported.</span></span>    |
|<span data-ttu-id="c13c7-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="c13c7-116">Application</span></span> | <span data-ttu-id="c13c7-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c13c7-117">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c13c7-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="c13c7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /groups/{id}/threads/{id}
PATCH /groups/{id}/conversations/{id}/threads/{id}

```
## <a name="request-headers"></a><span data-ttu-id="c13c7-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="c13c7-119">Request headers</span></span>
| <span data-ttu-id="c13c7-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c13c7-120">Header</span></span>       | <span data-ttu-id="c13c7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c13c7-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c13c7-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="c13c7-122">Authorization</span></span>  | <span data-ttu-id="c13c7-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="c13c7-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c13c7-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c13c7-125">Content-Type</span></span>  | <span data-ttu-id="c13c7-p104">application/json. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="c13c7-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c13c7-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="c13c7-128">Request body</span></span>
<span data-ttu-id="c13c7-p105">В тексте запроса укажите значения для соответствующих полей, которые необходимо обновить. Предыдущие значения существующих свойств, не включенных в текст запроса, останутся прежними или будут повторно вычислены с учетом измененных значений других свойств. Для достижения оптимальной производительности не следует включать существующие значения, которые не изменились.</span><span class="sxs-lookup"><span data-stu-id="c13c7-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c13c7-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="c13c7-132">Property</span></span>     | <span data-ttu-id="c13c7-133">Тип</span><span class="sxs-lookup"><span data-stu-id="c13c7-133">Type</span></span>   |<span data-ttu-id="c13c7-134">Описание</span><span class="sxs-lookup"><span data-stu-id="c13c7-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c13c7-135">isLocked</span><span class="sxs-lookup"><span data-stu-id="c13c7-135">isLocked</span></span>|<span data-ttu-id="c13c7-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="c13c7-136">Boolean</span></span>|<span data-ttu-id="c13c7-p106">Указывает, заблокирована ли цепочка. Чтобы запретить добавление сообщений, задайте значение `true`.</span><span class="sxs-lookup"><span data-stu-id="c13c7-p106">Indicates if the thread is locked. Set to `true` to disallow posting.</span></span>|

## <a name="response"></a><span data-ttu-id="c13c7-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="c13c7-139">Response</span></span>

<span data-ttu-id="c13c7-140">В случае успеха этот метод возвращает код отклика `200 OK` и обновленный объект [conversationThread](../resources/conversationthread.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="c13c7-140">If successful, this method returns a `200 OK` response code and updated [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c13c7-141">Пример</span><span class="sxs-lookup"><span data-stu-id="c13c7-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c13c7-142">Запрос</span><span class="sxs-lookup"><span data-stu-id="c13c7-142">Request</span></span>
<span data-ttu-id="c13c7-143">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="c13c7-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_conversationthread"
}-->
```http
PATCH https://graph.microsoft.com/beta/groups/{id}/threads/{id}
Content-type: application/json
Content-length: 419

{
  "@odata.type":"#Microsoft.OutlookServices.ConversationThread",
  "isLocked": true
}
```
##### <a name="response"></a><span data-ttu-id="c13c7-144">Ответ</span><span class="sxs-lookup"><span data-stu-id="c13c7-144">Response</span></span>
<span data-ttu-id="c13c7-p107">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
</span><span class="sxs-lookup"><span data-stu-id="c13c7-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 419

{
  "toRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ],
  "topic": "topic-value",
  "hasAttachments": true,
  "lastDeliveredDateTime": "2016-10-19T10:37:00Z",
  "uniqueSenders": [
    "uniqueSenders-value"
  ],
  "ccRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ],
  "isLocked": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update conversationthread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
