---
title: Создание Синчронизатионтемплате
description: Создайте новый шаблон синхронизации для конкретного приложения.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
ms.openlocfilehash: b5e9a3a9e90ef803f1c7a970edcb2c624b5196bc
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35869085"
---
# <a name="create-synchronizationtemplate"></a><span data-ttu-id="ba0e6-103">Создание Синчронизатионтемплате</span><span class="sxs-lookup"><span data-stu-id="ba0e6-103">Create synchronizationTemplate</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="ba0e6-104">Создайте новый шаблон синхронизации для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-104">Create a new synchronization template for a given application.</span></span>

## <a name="permissions"></a><span data-ttu-id="ba0e6-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="ba0e6-105">Permissions</span></span>
<span data-ttu-id="ba0e6-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba0e6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ba0e6-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="ba0e6-108">Permission type</span></span>                        | <span data-ttu-id="ba0e6-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="ba0e6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="ba0e6-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="ba0e6-110">Delegated (work or school account)</span></span>     |<span data-ttu-id="ba0e6-111">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ba0e6-111">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="ba0e6-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="ba0e6-112">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="ba0e6-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-113">Not supported.</span></span>|
|<span data-ttu-id="ba0e6-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="ba0e6-114">Application</span></span>                            |<span data-ttu-id="ba0e6-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-115">Not supported.</span></span>| 

### <a name="http-request"></a><span data-ttu-id="ba0e6-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="ba0e6-116">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /applications/{id}/synchronization/templates/
```

## <a name="request-headers"></a><span data-ttu-id="ba0e6-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="ba0e6-117">Request headers</span></span>

| <span data-ttu-id="ba0e6-118">Имя</span><span class="sxs-lookup"><span data-stu-id="ba0e6-118">Name</span></span>           | <span data-ttu-id="ba0e6-119">Тип</span><span class="sxs-lookup"><span data-stu-id="ba0e6-119">Type</span></span>    | <span data-ttu-id="ba0e6-120">Описание</span><span class="sxs-lookup"><span data-stu-id="ba0e6-120">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="ba0e6-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="ba0e6-121">Authorization</span></span>  | <span data-ttu-id="ba0e6-122">string</span><span class="sxs-lookup"><span data-stu-id="ba0e6-122">string</span></span>  | <span data-ttu-id="ba0e6-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ba0e6-125">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="ba0e6-125">Request body</span></span>

<span data-ttu-id="ba0e6-126">В теле запроса добавьте объект [синчронизатионтемплате](../resources/synchronization-synchronizationtemplate.md) , который требуется создать.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-126">In the request body, supply the [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) object to be created.</span></span> <span data-ttu-id="ba0e6-127">`id`Свойства `applicationId` и `factoryTag` свойства являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-127">The `id`, `applicationId` and `factoryTag` properties are required.</span></span> <span data-ttu-id="ba0e6-128">Если с `schema` шаблоном не предоставляется никакой шаблон, будет использоваться схема по умолчанию, связанная со `factoryTag` свойством.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-128">When no `schema` is provided with the template, the default schema associated with the `factoryTag` property will be used.</span></span>

### <a name="response"></a><span data-ttu-id="ba0e6-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="ba0e6-129">Response</span></span>

<span data-ttu-id="ba0e6-130">В случае успешного выполнения этот метод возвращает `201 Created` код отклика и объект [синчронизатионтемплате](../resources/synchronization-synchronizationtemplate.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-130">If successful, this method returns a `201 Created` response code and a [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) object in the response body.</span></span>

### <a name="example"></a><span data-ttu-id="ba0e6-131">Пример</span><span class="sxs-lookup"><span data-stu-id="ba0e6-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="ba0e6-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="ba0e6-132">Request</span></span>
<span data-ttu-id="ba0e6-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-133">The following is an example of a request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="ba0e6-134">HTTP</span><span class="sxs-lookup"><span data-stu-id="ba0e6-134">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_synchronizationtemplate_from_synchronization"
}-->
```http
POST https://graph.microsoft.com/beta/applications/{id}/synchronization/templates
Content-type: application/json

{ 
    "id": "SCIM-Test1",
    "applicationId": "{id}",
    "factoryTag": "CustomSCIM"
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="ba0e6-135">C#</span><span class="sxs-lookup"><span data-stu-id="ba0e6-135">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-synchronizationtemplate-from-synchronization-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="ba0e6-136">Javascript</span><span class="sxs-lookup"><span data-stu-id="ba0e6-136">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-synchronizationtemplate-from-synchronization-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="ba0e6-137">Цель — C</span><span class="sxs-lookup"><span data-stu-id="ba0e6-137">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-synchronizationtemplate-from-synchronization-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="ba0e6-138">Java</span><span class="sxs-lookup"><span data-stu-id="ba0e6-138">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/create-synchronizationtemplate-from-synchronization-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="ba0e6-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="ba0e6-139">Response</span></span>
<span data-ttu-id="ba0e6-140">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-140">The following is an example of a response.</span></span>
><span data-ttu-id="ba0e6-141">**Примечание.** Объект отклика, показанный здесь, может быть сокращен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-141">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="ba0e6-142">При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-142">All the properties will be returned in an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.synchronizationTemplate"
} -->
```http
HTTP/1.1 201 Created

{
    "id": "SCIM-Test1",
    "applicationId": "{id}",
    "factoryTag": "CustomSCIM",
    "schema": {
        "directories": [],
        "synchronizationRules": []
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create synchronizationTemplate",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
