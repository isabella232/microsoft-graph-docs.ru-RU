---
title: Запуск Синчронизатионжоб
description: Запуск существующего задания синхронизации. Если задание приостановлено, оно продолжит обработку изменений с того места, где оно было приостановлено. Если задание находится в карантине, состояние карантина будет очищено.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
ms.openlocfilehash: a06edb983a4efd1ccbd9ab7a6f2f3f88507a2181
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35869301"
---
# <a name="start-synchronizationjob"></a><span data-ttu-id="d6b75-105">Запуск Синчронизатионжоб</span><span class="sxs-lookup"><span data-stu-id="d6b75-105">Start synchronizationJob</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="d6b75-106">Запуск существующего задания синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d6b75-106">Start an existing synchronization job.</span></span> <span data-ttu-id="d6b75-107">Если задание приостановлено, оно продолжит обработку изменений с того места, где оно было приостановлено.</span><span class="sxs-lookup"><span data-stu-id="d6b75-107">If the job is in a paused state, it will continue processing changes from the point where it was paused.</span></span> <span data-ttu-id="d6b75-108">Если задание находится в карантине, состояние карантина будет очищено.</span><span class="sxs-lookup"><span data-stu-id="d6b75-108">If the job is in quarantine, the quarantine status will be cleared.</span></span>

## <a name="permissions"></a><span data-ttu-id="d6b75-109">Разрешения</span><span class="sxs-lookup"><span data-stu-id="d6b75-109">Permissions</span></span>
<span data-ttu-id="d6b75-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d6b75-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d6b75-112">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="d6b75-112">Permission type</span></span>                        | <span data-ttu-id="d6b75-113">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="d6b75-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="d6b75-114">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d6b75-114">Delegated (work or school account)</span></span>     |<span data-ttu-id="d6b75-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d6b75-115">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="d6b75-116">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="d6b75-116">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="d6b75-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d6b75-117">Not supported.</span></span> |
|<span data-ttu-id="d6b75-118">Для приложений</span><span class="sxs-lookup"><span data-stu-id="d6b75-118">Application</span></span>                            |<span data-ttu-id="d6b75-119">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d6b75-119">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="d6b75-120">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="d6b75-120">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/synchronization/jobs/{jobId}/start
```

## <a name="request-headers"></a><span data-ttu-id="d6b75-121">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="d6b75-121">Request headers</span></span>

| <span data-ttu-id="d6b75-122">Имя</span><span class="sxs-lookup"><span data-stu-id="d6b75-122">Name</span></span>           | <span data-ttu-id="d6b75-123">Тип</span><span class="sxs-lookup"><span data-stu-id="d6b75-123">Type</span></span>    | <span data-ttu-id="d6b75-124">Описание</span><span class="sxs-lookup"><span data-stu-id="d6b75-124">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="d6b75-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="d6b75-125">Authorization</span></span>  | <span data-ttu-id="d6b75-126">string</span><span class="sxs-lookup"><span data-stu-id="d6b75-126">string</span></span>  | <span data-ttu-id="d6b75-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d6b75-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d6b75-129">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="d6b75-129">Request body</span></span>

<span data-ttu-id="d6b75-130">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="d6b75-130">Do not supply a request body for this method.</span></span> 

## <a name="response"></a><span data-ttu-id="d6b75-131">Отклик</span><span class="sxs-lookup"><span data-stu-id="d6b75-131">Response</span></span>

<span data-ttu-id="d6b75-132">В случае успеха возвращает `204 No Content` отклик.</span><span class="sxs-lookup"><span data-stu-id="d6b75-132">If successful, returns a `204 No Content` response.</span></span> <span data-ttu-id="d6b75-133">В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="d6b75-133">It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d6b75-134">Пример</span><span class="sxs-lookup"><span data-stu-id="d6b75-134">Example</span></span>

##### <a name="request"></a><span data-ttu-id="d6b75-135">Запрос</span><span class="sxs-lookup"><span data-stu-id="d6b75-135">Request</span></span>
<span data-ttu-id="d6b75-136">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="d6b75-136">The following is an example of a request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="d6b75-137">HTTP</span><span class="sxs-lookup"><span data-stu-id="d6b75-137">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "synchronizationjob_start"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/start
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="d6b75-138">C#</span><span class="sxs-lookup"><span data-stu-id="d6b75-138">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/synchronizationjob-start-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="d6b75-139">Javascript</span><span class="sxs-lookup"><span data-stu-id="d6b75-139">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/synchronizationjob-start-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="d6b75-140">Цель — C</span><span class="sxs-lookup"><span data-stu-id="d6b75-140">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/synchronizationjob-start-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="d6b75-141">Java</span><span class="sxs-lookup"><span data-stu-id="d6b75-141">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/synchronizationjob-start-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="d6b75-142">Отклик</span><span class="sxs-lookup"><span data-stu-id="d6b75-142">Response</span></span>
<span data-ttu-id="d6b75-143">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="d6b75-143">The following is an example of a response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "synchronizationJob: start",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
