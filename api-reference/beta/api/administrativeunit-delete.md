---
title: Удаление administrativeUnit
description: Удаление administrativeUnit.
author: davidmu1
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 518b3545450a2aa6a3676d3cae19dccf06750b79
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42441769"
---
# <a name="delete-administrativeunit"></a><span data-ttu-id="c4434-103">Удаление administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="c4434-103">Delete administrativeUnit</span></span>

<span data-ttu-id="c4434-104">Пространство имен: Microsoft. Graph</span><span class="sxs-lookup"><span data-stu-id="c4434-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="c4434-105">Удаление [administrativeUnit](../resources/administrativeunit.md).</span><span class="sxs-lookup"><span data-stu-id="c4434-105">Delete an [administrativeUnit](../resources/administrativeunit.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="c4434-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="c4434-106">Permissions</span></span>
<span data-ttu-id="c4434-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c4434-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c4434-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="c4434-109">Permission type</span></span>      | <span data-ttu-id="c4434-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="c4434-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c4434-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c4434-111">Delegated (work or school account)</span></span> | <span data-ttu-id="c4434-112">AdministrativeUnit. ReadWrite. ALL, Directory. AccessAsUser. ALL</span><span class="sxs-lookup"><span data-stu-id="c4434-112">AdministrativeUnit.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c4434-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="c4434-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c4434-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c4434-114">Not supported.</span></span>    |
|<span data-ttu-id="c4434-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="c4434-115">Application</span></span> | <span data-ttu-id="c4434-116">AdministrativeUnit.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c4434-116">AdministrativeUnit.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c4434-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="c4434-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /administrativeUnits/{id}

```
## <a name="request-headers"></a><span data-ttu-id="c4434-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="c4434-118">Request headers</span></span>
| <span data-ttu-id="c4434-119">Имя</span><span class="sxs-lookup"><span data-stu-id="c4434-119">Name</span></span>       | <span data-ttu-id="c4434-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c4434-120">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c4434-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="c4434-121">Authorization</span></span>  | <span data-ttu-id="c4434-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="c4434-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c4434-124">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="c4434-124">Request body</span></span>
<span data-ttu-id="c4434-125">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="c4434-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c4434-126">Ответ</span><span class="sxs-lookup"><span data-stu-id="c4434-126">Response</span></span>

<span data-ttu-id="c4434-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="c4434-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c4434-129">Пример</span><span class="sxs-lookup"><span data-stu-id="c4434-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c4434-130">Запрос</span><span class="sxs-lookup"><span data-stu-id="c4434-130">Request</span></span>
<span data-ttu-id="c4434-131">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="c4434-131">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="c4434-132">HTTP</span><span class="sxs-lookup"><span data-stu-id="c4434-132">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_administrativeunit"
}-->
```http
DELETE https://graph.microsoft.com/beta/administrativeUnits/{id}
```
# <a name="c"></a>[<span data-ttu-id="c4434-133">C#</span><span class="sxs-lookup"><span data-stu-id="c4434-133">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-administrativeunit-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="c4434-134">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c4434-134">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-administrativeunit-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="c4434-135">Objective-C</span><span class="sxs-lookup"><span data-stu-id="c4434-135">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-administrativeunit-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a><span data-ttu-id="c4434-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="c4434-136">Response</span></span>
<span data-ttu-id="c4434-p104">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="c4434-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete administrativeUnit",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
