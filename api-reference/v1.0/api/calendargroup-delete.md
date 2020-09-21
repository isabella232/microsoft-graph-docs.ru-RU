---
title: Удаление объекта calendarGroup
description: Удаление группы календарей, отличной от стандартной.
author: harini84
localization_priority: Normal
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: bee626f15477984771295d3e3c51d2b1fc9b4877
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48070291"
---
# <a name="delete-calendargroup"></a><span data-ttu-id="f1e91-103">Удаление объекта calendarGroup</span><span class="sxs-lookup"><span data-stu-id="f1e91-103">Delete calendarGroup</span></span>

<span data-ttu-id="f1e91-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="f1e91-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="f1e91-105">Удаление группы календарей, отличной от стандартной.</span><span class="sxs-lookup"><span data-stu-id="f1e91-105">Delete a calendar group other than the default calendar group.</span></span>

## <a name="permissions"></a><span data-ttu-id="f1e91-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="f1e91-106">Permissions</span></span>

<span data-ttu-id="f1e91-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f1e91-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="f1e91-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="f1e91-109">Permission type</span></span>                        | <span data-ttu-id="f1e91-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="f1e91-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="f1e91-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="f1e91-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="f1e91-112">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f1e91-112">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="f1e91-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="f1e91-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f1e91-114">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f1e91-114">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="f1e91-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="f1e91-115">Application</span></span>                            | <span data-ttu-id="f1e91-116">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f1e91-116">Calendars.ReadWrite</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="f1e91-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="f1e91-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/calendarGroups/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="f1e91-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="f1e91-118">Request headers</span></span>

| <span data-ttu-id="f1e91-119">Имя</span><span class="sxs-lookup"><span data-stu-id="f1e91-119">Name</span></span>          | <span data-ttu-id="f1e91-120">Тип</span><span class="sxs-lookup"><span data-stu-id="f1e91-120">Type</span></span>   | <span data-ttu-id="f1e91-121">Описание</span><span class="sxs-lookup"><span data-stu-id="f1e91-121">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="f1e91-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f1e91-122">Authorization</span></span> | <span data-ttu-id="f1e91-123">string</span><span class="sxs-lookup"><span data-stu-id="f1e91-123">string</span></span> | <span data-ttu-id="f1e91-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="f1e91-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f1e91-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="f1e91-126">Request body</span></span>

<span data-ttu-id="f1e91-127">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="f1e91-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f1e91-128">Отклик</span><span class="sxs-lookup"><span data-stu-id="f1e91-128">Response</span></span>

<span data-ttu-id="f1e91-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="f1e91-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f1e91-131">Пример</span><span class="sxs-lookup"><span data-stu-id="f1e91-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="f1e91-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="f1e91-132">Request</span></span>

<span data-ttu-id="f1e91-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="f1e91-133">Here is an example of the request.</span></span>


# <a name="http"></a>[<span data-ttu-id="f1e91-134">HTTP</span><span class="sxs-lookup"><span data-stu-id="f1e91-134">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_calendargroup"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
```
# <a name="c"></a>[<span data-ttu-id="f1e91-135">C#</span><span class="sxs-lookup"><span data-stu-id="f1e91-135">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-calendargroup-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="f1e91-136">JavaScript</span><span class="sxs-lookup"><span data-stu-id="f1e91-136">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-calendargroup-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="f1e91-137">Objective-C</span><span class="sxs-lookup"><span data-stu-id="f1e91-137">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-calendargroup-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="f1e91-138">Java</span><span class="sxs-lookup"><span data-stu-id="f1e91-138">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-calendargroup-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="f1e91-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="f1e91-139">Response</span></span>

<span data-ttu-id="f1e91-p104">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="f1e91-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
  "description": "Delete calendarGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->

