---
title: Удаление объекта calendarGroup
description: Удаление группы календарей, отличной от стандартной.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 8a5ac7d57216806760f08ae6dd8daa7f5cc8995d
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35865023"
---
# <a name="delete-calendargroup"></a><span data-ttu-id="17e63-103">Удаление объекта calendarGroup</span><span class="sxs-lookup"><span data-stu-id="17e63-103">Delete calendarGroup</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="17e63-104">Удаление группы календарей, отличной от стандартной.</span><span class="sxs-lookup"><span data-stu-id="17e63-104">Delete a calendar group other than the default calendar group.</span></span>

## <a name="permissions"></a><span data-ttu-id="17e63-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="17e63-105">Permissions</span></span>

<span data-ttu-id="17e63-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="17e63-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="17e63-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="17e63-108">Permission type</span></span>                        | <span data-ttu-id="17e63-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="17e63-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="17e63-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="17e63-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="17e63-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="17e63-111">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="17e63-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="17e63-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="17e63-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="17e63-113">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="17e63-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="17e63-114">Application</span></span>                            | <span data-ttu-id="17e63-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="17e63-115">Calendars.ReadWrite</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="17e63-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="17e63-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/calendarGroups/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="17e63-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="17e63-117">Request headers</span></span>

| <span data-ttu-id="17e63-118">Имя</span><span class="sxs-lookup"><span data-stu-id="17e63-118">Name</span></span>          | <span data-ttu-id="17e63-119">Тип</span><span class="sxs-lookup"><span data-stu-id="17e63-119">Type</span></span>   | <span data-ttu-id="17e63-120">Описание</span><span class="sxs-lookup"><span data-stu-id="17e63-120">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="17e63-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="17e63-121">Authorization</span></span> | <span data-ttu-id="17e63-122">string</span><span class="sxs-lookup"><span data-stu-id="17e63-122">string</span></span> | <span data-ttu-id="17e63-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="17e63-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="17e63-125">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="17e63-125">Request body</span></span>

<span data-ttu-id="17e63-126">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="17e63-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="17e63-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="17e63-127">Response</span></span>

<span data-ttu-id="17e63-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="17e63-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="17e63-130">Пример</span><span class="sxs-lookup"><span data-stu-id="17e63-130">Example</span></span>

##### <a name="request"></a><span data-ttu-id="17e63-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="17e63-131">Request</span></span>

<span data-ttu-id="17e63-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="17e63-132">Here is an example of the request.</span></span>


# <a name="httptabhttp"></a>[<span data-ttu-id="17e63-133">HTTP</span><span class="sxs-lookup"><span data-stu-id="17e63-133">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_calendargroup"
}-->

```http
DELETE https://graph.microsoft.com/beta/me/calendarGroups/{id}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="17e63-134">C#</span><span class="sxs-lookup"><span data-stu-id="17e63-134">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-calendargroup-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="17e63-135">Javascript</span><span class="sxs-lookup"><span data-stu-id="17e63-135">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-calendargroup-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="17e63-136">Цель — C</span><span class="sxs-lookup"><span data-stu-id="17e63-136">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-calendargroup-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="17e63-137">Java</span><span class="sxs-lookup"><span data-stu-id="17e63-137">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-calendargroup-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="17e63-138">Отклик</span><span class="sxs-lookup"><span data-stu-id="17e63-138">Response</span></span>

<span data-ttu-id="17e63-p104">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="17e63-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!--
{
  "type": "#page.annotation",
  "description": "Delete calendarGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
