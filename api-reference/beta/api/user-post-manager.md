---
title: Назначение руководителя
description: С помощью этого API можно назначить руководителя пользователю.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: dbfae1400d5b67f968f61779295eab7c2b3144cf
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42451688"
---
# <a name="assign-a-manager"></a><span data-ttu-id="6fd45-103">Назначение руководителя</span><span class="sxs-lookup"><span data-stu-id="6fd45-103">Assign a manager</span></span>

<span data-ttu-id="6fd45-104">Пространство имен: Microsoft. Graph</span><span class="sxs-lookup"><span data-stu-id="6fd45-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="6fd45-105">С помощью этого API можно назначить руководителя пользователю.</span><span class="sxs-lookup"><span data-stu-id="6fd45-105">Use this API to assign a user's manager.</span></span>
> <span data-ttu-id="6fd45-106">Примечание. Назначать подчиненных невозможно. Вместо этого используйте данный API.</span><span class="sxs-lookup"><span data-stu-id="6fd45-106">Note: You cannot assign direct reports - instead use this API.</span></span>

## <a name="permissions"></a><span data-ttu-id="6fd45-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="6fd45-107">Permissions</span></span>
<span data-ttu-id="6fd45-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6fd45-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6fd45-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="6fd45-110">Permission type</span></span>      | <span data-ttu-id="6fd45-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="6fd45-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6fd45-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6fd45-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6fd45-113">User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6fd45-113">User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="6fd45-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="6fd45-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6fd45-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6fd45-115">Not supported.</span></span>    |
|<span data-ttu-id="6fd45-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="6fd45-116">Application</span></span> | <span data-ttu-id="6fd45-117">User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6fd45-117">User.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6fd45-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="6fd45-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /users/{id}/manager/$ref
```
## <a name="request-headers"></a><span data-ttu-id="6fd45-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="6fd45-119">Request headers</span></span>
| <span data-ttu-id="6fd45-120">Имя</span><span class="sxs-lookup"><span data-stu-id="6fd45-120">Name</span></span>       | <span data-ttu-id="6fd45-121">Тип</span><span class="sxs-lookup"><span data-stu-id="6fd45-121">Type</span></span> | <span data-ttu-id="6fd45-122">Описание</span><span class="sxs-lookup"><span data-stu-id="6fd45-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6fd45-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6fd45-123">Authorization</span></span>  | <span data-ttu-id="6fd45-124">string</span><span class="sxs-lookup"><span data-stu-id="6fd45-124">string</span></span>  | <span data-ttu-id="6fd45-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6fd45-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6fd45-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="6fd45-127">Request body</span></span>
<span data-ttu-id="6fd45-128">Предоставьте в тексте запроса описание добавляемого объекта [directoryObject](../resources/directoryobject.md) или [user](../resources/user.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="6fd45-128">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) or [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="6fd45-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="6fd45-129">Response</span></span>

<span data-ttu-id="6fd45-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="6fd45-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6fd45-132">Пример</span><span class="sxs-lookup"><span data-stu-id="6fd45-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6fd45-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="6fd45-133">Request</span></span>
<span data-ttu-id="6fd45-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="6fd45-134">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="6fd45-135">HTTP</span><span class="sxs-lookup"><span data-stu-id="6fd45-135">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_manager_for_user"
}-->
```http
PUT https://graph.microsoft.com/v1.0/users/{id}/manager/$ref
Content-type: application/json
Content-length: xxx

{
  "@odata.id": "https://graph.microsoft.com/v1.0/users/{id}"
}
```
# <a name="c"></a>[<span data-ttu-id="6fd45-136">C#</span><span class="sxs-lookup"><span data-stu-id="6fd45-136">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-manager-for-user-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="6fd45-137">JavaScript</span><span class="sxs-lookup"><span data-stu-id="6fd45-137">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-manager-for-user-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="6fd45-138">Objective-C</span><span class="sxs-lookup"><span data-stu-id="6fd45-138">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-manager-for-user-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="6fd45-139">Java</span><span class="sxs-lookup"><span data-stu-id="6fd45-139">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/create-manager-for-user-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

<span data-ttu-id="6fd45-140">Предоставьте в тексте запроса описание добавляемого объекта [user](../resources/user.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="6fd45-140">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>
##### <a name="response"></a><span data-ttu-id="6fd45-141">Отклик</span><span class="sxs-lookup"><span data-stu-id="6fd45-141">Response</span></span>
<span data-ttu-id="6fd45-p104">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="6fd45-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create member",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
