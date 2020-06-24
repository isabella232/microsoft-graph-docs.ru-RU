---
title: Удаление schemaExtension
description: Удаление определения расширения схемы.
localization_priority: Normal
author: dkershaw10
doc_type: apiPageType
ms.prod: extensions
ms.openlocfilehash: f8e5d78d0f23430bbd693832a918374af736d1bd
ms.sourcegitcommit: 1ec5a7be90790aaebdf6d85d93ab0c72b381c9c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "44863497"
---
# <a name="delete-schemaextension"></a><span data-ttu-id="d6d78-103">Удаление schemaExtension</span><span class="sxs-lookup"><span data-stu-id="d6d78-103">Delete schemaExtension</span></span>

<span data-ttu-id="d6d78-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="d6d78-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="d6d78-105">Удаление определения [расширения схемы](../resources/schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="d6d78-105">Delete the definition of a [schema extension](../resources/schemaextension.md).</span></span>

<span data-ttu-id="d6d78-106">Only the app that created the schema extension (owner app) can delete the schema extension definition, and only when the extension is in the **InDevelopment** state.</span><span class="sxs-lookup"><span data-stu-id="d6d78-106">Only the app that created the schema extension (owner app) can delete the schema extension definition, and only when the extension is in the **InDevelopment** state.</span></span> <span data-ttu-id="d6d78-107">Deleting a schema extension definition does not affect accessing custom data that has been added to resource instances based on that definition.</span><span class="sxs-lookup"><span data-stu-id="d6d78-107">Deleting a schema extension definition does not affect accessing custom data that has been added to resource instances based on that definition.</span></span>


## <a name="permissions"></a><span data-ttu-id="d6d78-108">Разрешения</span><span class="sxs-lookup"><span data-stu-id="d6d78-108">Permissions</span></span>
<span data-ttu-id="d6d78-109">One of the following permissions is required to call this API.</span><span class="sxs-lookup"><span data-stu-id="d6d78-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="d6d78-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d6d78-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="d6d78-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="d6d78-111">Permission type</span></span>      | <span data-ttu-id="d6d78-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="d6d78-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d6d78-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d6d78-113">Delegated (work or school account)</span></span> | <span data-ttu-id="d6d78-114">Application. ReadWrite. ALL, Directory. AccessAsUser. ALL</span><span class="sxs-lookup"><span data-stu-id="d6d78-114">Application.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="d6d78-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="d6d78-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d6d78-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d6d78-116">Not supported.</span></span>    |
|<span data-ttu-id="d6d78-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="d6d78-117">Application</span></span> | <span data-ttu-id="d6d78-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d6d78-118">Not supported.</span></span> |

> [!NOTE]
> <span data-ttu-id="d6d78-119">Кроме того, для делегированного процесса вошедшего в систему пользователя можно удалить только schemaExtensions, которыми они владеют (где свойство **owner** объекта schemaExtension — это `appId` приложение, которому принадлежит вошедшего пользователь).</span><span class="sxs-lookup"><span data-stu-id="d6d78-119">Additionally for the delegated flow, the signed-in user can only delete schemaExtensions they own (where the **owner** property of the schemaExtension is the `appId` of an application the signed-in user owns).</span></span>

## <a name="http-request"></a><span data-ttu-id="d6d78-120">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="d6d78-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /schemaExtensions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="d6d78-121">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="d6d78-121">Request headers</span></span>
| <span data-ttu-id="d6d78-122">Имя</span><span class="sxs-lookup"><span data-stu-id="d6d78-122">Name</span></span>      |<span data-ttu-id="d6d78-123">Описание</span><span class="sxs-lookup"><span data-stu-id="d6d78-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d6d78-124">Авторизация</span><span class="sxs-lookup"><span data-stu-id="d6d78-124">Authorization</span></span>  | <span data-ttu-id="d6d78-125">Bearer {token}.</span><span class="sxs-lookup"><span data-stu-id="d6d78-125">Bearer {token}.</span></span> <span data-ttu-id="d6d78-126">Required.</span><span class="sxs-lookup"><span data-stu-id="d6d78-126">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d6d78-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="d6d78-127">Request body</span></span>
<span data-ttu-id="d6d78-128">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="d6d78-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d6d78-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="d6d78-129">Response</span></span>

<span data-ttu-id="d6d78-130">If successful, this method returns `204 No Content` response code.</span><span class="sxs-lookup"><span data-stu-id="d6d78-130">If successful, this method returns `204 No Content` response code.</span></span> <span data-ttu-id="d6d78-131">It does not return anything in the response body.</span><span class="sxs-lookup"><span data-stu-id="d6d78-131">It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d6d78-132">Пример</span><span class="sxs-lookup"><span data-stu-id="d6d78-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d6d78-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="d6d78-133">Request</span></span>
<span data-ttu-id="d6d78-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="d6d78-134">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="d6d78-135">HTTP</span><span class="sxs-lookup"><span data-stu-id="d6d78-135">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_schemaextension"
}-->
```http
DELETE https://graph.microsoft.com/beta/schemaExtensions/{id}
```
# <a name="c"></a>[<span data-ttu-id="d6d78-136">C#</span><span class="sxs-lookup"><span data-stu-id="d6d78-136">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-schemaextension-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="d6d78-137">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d6d78-137">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-schemaextension-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="d6d78-138">Objective-C</span><span class="sxs-lookup"><span data-stu-id="d6d78-138">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-schemaextension-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="d6d78-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="d6d78-139">Response</span></span>
<span data-ttu-id="d6d78-140">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="d6d78-140">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="d6d78-141">См. также</span><span class="sxs-lookup"><span data-stu-id="d6d78-141">See also</span></span>

- [<span data-ttu-id="d6d78-142">Добавление пользовательских данных в ресурсы с помощью расширений</span><span class="sxs-lookup"><span data-stu-id="d6d78-142">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="d6d78-143">Добавление пользовательских данных в группы с помощью расширений схемы</span><span class="sxs-lookup"><span data-stu-id="d6d78-143">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Delete schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
