---
title: Добавление Конверсатионмембер
description: Добавление Конверсатионмембер к каналу.
author: clearab
doc_type: apiPageType
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: fd1f2c6689176422fa35a500224c6f2a5f277851
ms.sourcegitcommit: 0329bbcd5f1b09a2a6c5f935a30c4560b6eed492
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "36634053"
---
# <a name="add-conversationmember"></a><span data-ttu-id="d4d3e-103">Добавление Конверсатионмембер</span><span class="sxs-lookup"><span data-stu-id="d4d3e-103">Add conversationMember</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="d4d3e-104">Добавление [конверсатионмембер](../resources/conversationmember.md) к каналу [](../resources/channel.md).</span><span class="sxs-lookup"><span data-stu-id="d4d3e-104">Add a [conversationMember](../resources/conversationmember.md) to a [channel](../resources/channel.md).</span></span>

> [!NOTE]
><span data-ttu-id="d4d3e-105">Эта операция поддерживается только для каналов с [чаннелмембершиптипе](../resources/enums.md#channelmembershiptype-values) `private`.</span><span class="sxs-lookup"><span data-stu-id="d4d3e-105">This operation is only supported on channels with a [channelMembershipType](../resources/enums.md#channelmembershiptype-values) of `private`.</span></span> <span data-ttu-id="d4d3e-106">Вызовы с любыми другими [чаннелмембершиптипе](../resources/enums.md#channelmembershiptype-values) будут возвращать ответ о неправильном запросе 400.</span><span class="sxs-lookup"><span data-stu-id="d4d3e-106">Calls with any other [channelMembershipType](../resources/enums.md#channelmembershiptype-values) will return a 400 Bad Request response.</span></span>

## <a name="permissions"></a><span data-ttu-id="d4d3e-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="d4d3e-107">Permissions</span></span>

<span data-ttu-id="d4d3e-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, в том числе о выборе разрешений, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d4d3e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d4d3e-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="d4d3e-110">Permission Type</span></span>|<span data-ttu-id="d4d3e-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="d4d3e-111">Permissions (from least to most privileged)</span></span>|
|---------|-------------|
|<span data-ttu-id="d4d3e-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d4d3e-112">Delegated (work or school account)</span></span>|<span data-ttu-id="d4d3e-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d4d3e-113">Group.ReadWrite.All</span></span>|
|<span data-ttu-id="d4d3e-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="d4d3e-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d4d3e-115">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d4d3e-115">Not supported</span></span>|
|<span data-ttu-id="d4d3e-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="d4d3e-116">Application</span></span>|<span data-ttu-id="d4d3e-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d4d3e-117">Group.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="d4d3e-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="d4d3e-118">HTTP request</span></span>
<!-- { "blockType": "ignored"} -->
```http
POST /teams/{id}/channels/{id}/members/{id}
```

## <a name="request-headers"></a><span data-ttu-id="d4d3e-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="d4d3e-119">Request headers</span></span>

| <span data-ttu-id="d4d3e-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d4d3e-120">Header</span></span>       | <span data-ttu-id="d4d3e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d4d3e-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d4d3e-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="d4d3e-122">Authorization</span></span>  | <span data-ttu-id="d4d3e-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d4d3e-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d4d3e-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="d4d3e-125">Request body</span></span>

<span data-ttu-id="d4d3e-126">Включите в запрос указанные ниже свойства.</span><span class="sxs-lookup"><span data-stu-id="d4d3e-126">Include the following properties in the request body.</span></span>

| <span data-ttu-id="d4d3e-127">Свойство</span><span class="sxs-lookup"><span data-stu-id="d4d3e-127">Property</span></span>   | <span data-ttu-id="d4d3e-128">Тип</span><span class="sxs-lookup"><span data-stu-id="d4d3e-128">Type</span></span> |<span data-ttu-id="d4d3e-129">Описание</span><span class="sxs-lookup"><span data-stu-id="d4d3e-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d4d3e-130">roles</span><span class="sxs-lookup"><span data-stu-id="d4d3e-130">roles</span></span>|<span data-ttu-id="d4d3e-131">string collection</span><span class="sxs-lookup"><span data-stu-id="d4d3e-131">string collection</span></span>|<span data-ttu-id="d4d3e-132">Роли для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4d3e-132">The roles for that user.</span></span>|
|<span data-ttu-id="d4d3e-133">user</span><span class="sxs-lookup"><span data-stu-id="d4d3e-133">user</span></span>|[<span data-ttu-id="d4d3e-134">user</span><span class="sxs-lookup"><span data-stu-id="d4d3e-134">user</span></span>](../resources/user.md)|<span data-ttu-id="d4d3e-135">Пользователь, добавляемый в канал.</span><span class="sxs-lookup"><span data-stu-id="d4d3e-135">The user to add to the channel.</span></span>|

## <a name="response"></a><span data-ttu-id="d4d3e-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="d4d3e-136">Response</span></span>

<span data-ttu-id="d4d3e-137">В случае успешного выполнения этот метод возвращает `201 Created` код отклика и объект [конверсатионмембер](../resources/conversationmember.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="d4d3e-137">If successful, this method returns a `201 Created` response code and a [conversationMember](../resources/conversationmember.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d4d3e-138">Пример</span><span class="sxs-lookup"><span data-stu-id="d4d3e-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="d4d3e-139">Запрос</span><span class="sxs-lookup"><span data-stu-id="d4d3e-139">Request</span></span>

<span data-ttu-id="d4d3e-140">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="d4d3e-140">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="d4d3e-141">HTTP</span><span class="sxs-lookup"><span data-stu-id="d4d3e-141">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_conversation_member"
} -->
```http
POST https://graph.microsoft.com/beta/teams/{id}/channels/{id}/members/
content-type: application/json
content-length: 26

{
  "@odata.type": "microsoft.graph.aadConversationMember",
  "roles": [],
  "user@odata.bind": "https://graph.microsoft.com/beta/users/8b081ef6-4792-4def-b2c9-c363a1bf41d5"
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="d4d3e-142">C#</span><span class="sxs-lookup"><span data-stu-id="d4d3e-142">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-conversation-member-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="d4d3e-143">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d4d3e-143">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-conversation-member-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="d4d3e-144">Цель — C</span><span class="sxs-lookup"><span data-stu-id="d4d3e-144">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-conversation-member-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="d4d3e-145">Отклик</span><span class="sxs-lookup"><span data-stu-id="d4d3e-145">Response</span></span>

<span data-ttu-id="d4d3e-146">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="d4d3e-146">Here is an example of the response.</span></span>

><span data-ttu-id="d4d3e-p104">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="d4d3e-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationMember"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 468

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#teams('ece6f0a1-7ca4-498b-be79-edf6c8fc4d82')/channels('19%3A56eb04e133944cf69e603c5dac2d292e%40thread.skype')/members/microsoft.graph.aadUserConversationMember/$entity",
  "@odata.type": "#microsoft.graph.aadUserConversationMember",
  "id": "8b081ef6-4792-4def-b2c9-c363a1bf41d5",
  "roles": [],
  "displayName": "John Doe",
  "userId": "8b081ef6-4792-4def-b2c9-c363a1bf41d5",
  "email": null
}
```