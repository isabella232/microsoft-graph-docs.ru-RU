---
title: Удаление Линкедресаурце
description: Удаляет объект Линкедресаурце.
author: avijityadav
localization_priority: Normal
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: 5bf6ab3c6791e84602efc8eb0d61be8d825ec012
ms.sourcegitcommit: ef47b165f7a140cfc0309a275cb8722dd265660d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/25/2020
ms.locfileid: "46873331"
---
# <a name="delete-linkedresource"></a><span data-ttu-id="59895-103">Удаление Линкедресаурце</span><span class="sxs-lookup"><span data-stu-id="59895-103">Delete linkedResource</span></span>
<span data-ttu-id="59895-104">Пространство имен: Microsoft. Graph [!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]</span><span class="sxs-lookup"><span data-stu-id="59895-104">Namespace: microsoft.graph [!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]</span></span>

<span data-ttu-id="59895-105">Удаляет объект [линкедресаурце](../resources/linkedresource.md) .</span><span class="sxs-lookup"><span data-stu-id="59895-105">Deletes a [linkedResource](../resources/linkedresource.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="59895-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="59895-106">Permissions</span></span>
<span data-ttu-id="59895-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="59895-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="59895-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="59895-109">Permission type</span></span>|<span data-ttu-id="59895-110">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="59895-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="59895-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="59895-111">Delegated (work or school account)</span></span>|<span data-ttu-id="59895-112">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="59895-112">Tasks.ReadWrite</span></span>|
|<span data-ttu-id="59895-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="59895-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="59895-114">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="59895-114">Tasks.ReadWrite</span></span>|
|<span data-ttu-id="59895-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="59895-115">Application</span></span>|<span data-ttu-id="59895-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="59895-116">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="59895-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="59895-117">HTTP request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /me/todo/lists/{todoTaskListId}/tasks/{taskId}/linkedResources/{linkedResourcesId}
DELETE /users/{id|userPrincipalName}/todo/lists/{todoTaskListId}/tasks/{taskId}/linkedResources/{linkedResourcesId}
```

## <a name="request-headers"></a><span data-ttu-id="59895-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="59895-118">Request headers</span></span>
|<span data-ttu-id="59895-119">Имя</span><span class="sxs-lookup"><span data-stu-id="59895-119">Name</span></span>|<span data-ttu-id="59895-120">Описание</span><span class="sxs-lookup"><span data-stu-id="59895-120">Description</span></span>|
|:---|:---|
|<span data-ttu-id="59895-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="59895-121">Authorization</span></span>|<span data-ttu-id="59895-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="59895-p102">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="59895-124">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="59895-124">Request body</span></span>
<span data-ttu-id="59895-125">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="59895-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="59895-126">Отклик</span><span class="sxs-lookup"><span data-stu-id="59895-126">Response</span></span>

<span data-ttu-id="59895-127">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="59895-127">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="examples"></a><span data-ttu-id="59895-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="59895-128">Examples</span></span>

### <a name="request"></a><span data-ttu-id="59895-129">Запрос</span><span class="sxs-lookup"><span data-stu-id="59895-129">Request</span></span>

# <a name="http"></a>[<span data-ttu-id="59895-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="59895-130">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "sampleKeys": ["dfsdc-f9dfdfs-dcsda9", "e2dc-f9cce2-dce29", "f9cddce2-dce2-f9cd-e2dc-cdf9e2dccdf9"],
  "name": "delete_linkedresource"
}
-->
``` http
DELETE https://graph.microsoft.com/beta/me/todo/lists/dfsdc-f9dfdfs-dcsda9/tasks/e2dc-f9cce2-dce29/linkedResources/f9cddce2-dce2-f9cd-e2dc-cdf9e2dccdf9
```
# <a name="c"></a>[<span data-ttu-id="59895-131">C#</span><span class="sxs-lookup"><span data-stu-id="59895-131">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-linkedresource-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="59895-132">JavaScript</span><span class="sxs-lookup"><span data-stu-id="59895-132">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-linkedresource-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="59895-133">Objective-C</span><span class="sxs-lookup"><span data-stu-id="59895-133">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-linkedresource-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---



### <a name="response"></a><span data-ttu-id="59895-134">Отклик</span><span class="sxs-lookup"><span data-stu-id="59895-134">Response</span></span>
<span data-ttu-id="59895-135">**Примечание.** Объект отклика, показанный здесь, может быть сокращен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="59895-135">**Note:** The response object shown here might be shortened for readability.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```

