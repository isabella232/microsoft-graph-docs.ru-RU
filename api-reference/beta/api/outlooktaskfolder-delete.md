---
title: Удаление outlookTaskFolder
description: Удаление указанной папки задач Outlook.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: 00ab601344a3820e3fd96ef9753c124f263da6c4
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "36349826"
---
# <a name="delete-outlooktaskfolder"></a><span data-ttu-id="d5d6e-103">Удаление outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="d5d6e-103">Delete outlookTaskFolder</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="d5d6e-104">Удаление указанной папки задач Outlook.</span><span class="sxs-lookup"><span data-stu-id="d5d6e-104">Delete the specified Outlook task folder.</span></span>
## <a name="permissions"></a><span data-ttu-id="d5d6e-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="d5d6e-105">Permissions</span></span>
<span data-ttu-id="d5d6e-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d5d6e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d5d6e-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="d5d6e-108">Permission type</span></span>      | <span data-ttu-id="d5d6e-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="d5d6e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d5d6e-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d5d6e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d5d6e-111">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5d6e-111">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="d5d6e-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="d5d6e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d5d6e-113">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5d6e-113">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="d5d6e-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="d5d6e-114">Application</span></span> | <span data-ttu-id="d5d6e-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d5d6e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d5d6e-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="d5d6e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/outlook/taskFolders/{id}
DELETE /me/outlook/taskGroups/{id}/taskFolders/{id}
DELETE /users/{id|userPrincipalName}/outlook/taskFolders/{id}
DELETE /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="d5d6e-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="d5d6e-117">Request headers</span></span>
| <span data-ttu-id="d5d6e-118">Имя</span><span class="sxs-lookup"><span data-stu-id="d5d6e-118">Name</span></span>       | <span data-ttu-id="d5d6e-119">Описание</span><span class="sxs-lookup"><span data-stu-id="d5d6e-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d5d6e-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="d5d6e-120">Authorization</span></span>  | <span data-ttu-id="d5d6e-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d5d6e-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d5d6e-123">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="d5d6e-123">Request body</span></span>
<span data-ttu-id="d5d6e-124">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="d5d6e-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d5d6e-125">Отклик</span><span class="sxs-lookup"><span data-stu-id="d5d6e-125">Response</span></span>

<span data-ttu-id="d5d6e-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="d5d6e-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d5d6e-128">Пример</span><span class="sxs-lookup"><span data-stu-id="d5d6e-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d5d6e-129">Запрос</span><span class="sxs-lookup"><span data-stu-id="d5d6e-129">Request</span></span>
<span data-ttu-id="d5d6e-130">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="d5d6e-130">Here is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="d5d6e-131">HTTP</span><span class="sxs-lookup"><span data-stu-id="d5d6e-131">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_outlooktaskfolder"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/outlook/taskFolders/AAMkADIyAAAhrbPXAAA=
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="d5d6e-132">C#</span><span class="sxs-lookup"><span data-stu-id="d5d6e-132">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-outlooktaskfolder-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="d5d6e-133">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d5d6e-133">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-outlooktaskfolder-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="d5d6e-134">Цель — C</span><span class="sxs-lookup"><span data-stu-id="d5d6e-134">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-outlooktaskfolder-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="d5d6e-135">Java</span><span class="sxs-lookup"><span data-stu-id="d5d6e-135">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-outlooktaskfolder-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="d5d6e-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="d5d6e-136">Response</span></span>
<span data-ttu-id="d5d6e-137">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="d5d6e-137">Here is an example of the response.</span></span> 
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
  "description": "Delete outlookTaskFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
