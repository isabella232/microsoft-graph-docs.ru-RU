---
title: Создание объекта acceptedSender
description: Добавление пользователя или группы в список объектов acceptedSender.
ms.openlocfilehash: 4a3cfd89d37a18cbb85644b2c4adc71470950235
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27027753"
---
# <a name="create-acceptedsender"></a><span data-ttu-id="7d338-103">Создание объекта acceptedSender</span><span class="sxs-lookup"><span data-stu-id="7d338-103">Create acceptedSender</span></span>
<span data-ttu-id="7d338-104">Добавление пользователя или группы в список объектов acceptedSender.</span><span class="sxs-lookup"><span data-stu-id="7d338-104">Add a new user or group to the acceptedSender list.</span></span>

<span data-ttu-id="7d338-p101">Укажите пользователя или группу с помощью параметра `@odata.id` в тексте запроса. Пользователи из списка разрешенных отправителей могут отправлять записи в беседы группы. Убедитесь, что в списках разрешенных и запрещенных отправителей не указаны одни и те же пользователи или группы. В противном случае возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7d338-p101">Specify the user or group in `@odata.id` in the request body. Users in the accepted senders list can post to conversations of the group . Make sure you do not specify the same user or group in the accepted senders and rejected senders lists, otherwise you will get an error.</span></span>

## <a name="permissions"></a><span data-ttu-id="7d338-108">Разрешения</span><span class="sxs-lookup"><span data-stu-id="7d338-108">Permissions</span></span>
<span data-ttu-id="7d338-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7d338-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7d338-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="7d338-111">Permission type</span></span>      | <span data-ttu-id="7d338-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="7d338-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7d338-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7d338-113">Delegated (work or school account)</span></span> | <span data-ttu-id="7d338-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d338-114">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="7d338-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="7d338-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7d338-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d338-116">Not supported.</span></span>    |
|<span data-ttu-id="7d338-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="7d338-117">Application</span></span> | <span data-ttu-id="7d338-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d338-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7d338-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="7d338-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/acceptedSenders/$ref
```
## <a name="request-headers"></a><span data-ttu-id="7d338-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="7d338-120">Request headers</span></span>
| <span data-ttu-id="7d338-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7d338-121">Header</span></span>       | <span data-ttu-id="7d338-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7d338-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7d338-123">Авторизация</span><span class="sxs-lookup"><span data-stu-id="7d338-123">Authorization</span></span>  | <span data-ttu-id="7d338-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7d338-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7d338-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="7d338-126">Request body</span></span>
<span data-ttu-id="7d338-127">Укажите в тексте запроса идентификатор объекта user или group.</span><span class="sxs-lookup"><span data-stu-id="7d338-127">In the request body, supply the id of a user or group object.</span></span>

## <a name="response"></a><span data-ttu-id="7d338-128">Отклик</span><span class="sxs-lookup"><span data-stu-id="7d338-128">Response</span></span>
<span data-ttu-id="7d338-129">Этот метод возвращает код отклика `204 No Content`, но не возвращает текст отклика.</span><span class="sxs-lookup"><span data-stu-id="7d338-129">This method returns `204 No Content` response code and no response body.</span></span>

## <a name="example"></a><span data-ttu-id="7d338-130">Пример</span><span class="sxs-lookup"><span data-stu-id="7d338-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="7d338-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="7d338-131">Request</span></span>
<span data-ttu-id="7d338-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="7d338-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_acceptedsender"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id":"https://graph.microsoft.com/v1.0/users/alexd@contoso.com"
}
```

#### <a name="response"></a><span data-ttu-id="7d338-133">Ответ</span><span class="sxs-lookup"><span data-stu-id="7d338-133">Response</span></span>
<span data-ttu-id="7d338-134">Ниже приведен пример ответа.</span><span class="sxs-lookup"><span data-stu-id="7d338-134">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create acceptedSender",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
