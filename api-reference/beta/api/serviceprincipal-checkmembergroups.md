---
title: 'servicePrincipal: Чеккмемберграупс'
description: Для вызова этого API требуется одно из следующих разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье Разрешения.
localization_priority: Normal
doc_type: apiPageType
ms.prod: microsoft-identity-platform
author: sureshja
ms.openlocfilehash: 120cd98ea22a452593e41f93637211151d1d1f2b
ms.sourcegitcommit: bdef75943ade3f1080120f555b67d5ebb3245699
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/10/2020
ms.locfileid: "43219342"
---
# <a name="serviceprincipal-checkmembergroups"></a><span data-ttu-id="e1840-104">servicePrincipal: Чеккмемберграупс</span><span class="sxs-lookup"><span data-stu-id="e1840-104">servicePrincipal: checkMemberGroups</span></span>

<span data-ttu-id="e1840-105">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="e1840-105">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

## <a name="permissions"></a><span data-ttu-id="e1840-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="e1840-106">Permissions</span></span>
<span data-ttu-id="e1840-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e1840-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e1840-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="e1840-109">Permission type</span></span>      | <span data-ttu-id="e1840-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="e1840-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e1840-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="e1840-111">Delegated (work or school account)</span></span> | <span data-ttu-id="e1840-112">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e1840-112">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="e1840-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="e1840-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e1840-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e1840-114">Not supported.</span></span>    |
|<span data-ttu-id="e1840-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="e1840-115">Application</span></span> | <span data-ttu-id="e1840-116">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="e1840-116">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e1840-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="e1840-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/checkMemberGroups

```
## <a name="request-headers"></a><span data-ttu-id="e1840-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="e1840-118">Request headers</span></span>
| <span data-ttu-id="e1840-119">Имя</span><span class="sxs-lookup"><span data-stu-id="e1840-119">Name</span></span>       | <span data-ttu-id="e1840-120">Тип</span><span class="sxs-lookup"><span data-stu-id="e1840-120">Type</span></span> | <span data-ttu-id="e1840-121">Описание</span><span class="sxs-lookup"><span data-stu-id="e1840-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e1840-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e1840-122">Authorization</span></span>  | <span data-ttu-id="e1840-123">string</span><span class="sxs-lookup"><span data-stu-id="e1840-123">string</span></span>  | <span data-ttu-id="e1840-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e1840-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e1840-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="e1840-126">Request body</span></span>
<span data-ttu-id="e1840-127">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="e1840-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="e1840-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="e1840-128">Parameter</span></span>    | <span data-ttu-id="e1840-129">Тип</span><span class="sxs-lookup"><span data-stu-id="e1840-129">Type</span></span>   |<span data-ttu-id="e1840-130">Описание</span><span class="sxs-lookup"><span data-stu-id="e1840-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e1840-131">groupIds</span><span class="sxs-lookup"><span data-stu-id="e1840-131">groupIds</span></span>|<span data-ttu-id="e1840-132">Коллекция строк</span><span class="sxs-lookup"><span data-stu-id="e1840-132">String collection</span></span>||

## <a name="response"></a><span data-ttu-id="e1840-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="e1840-133">Response</span></span>

<span data-ttu-id="e1840-134">В случае успеха этот метод возвращает код отклика `200 OK` и объект коллекции String в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="e1840-134">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e1840-135">Пример</span><span class="sxs-lookup"><span data-stu-id="e1840-135">Example</span></span>
<span data-ttu-id="e1840-136">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="e1840-136">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e1840-137">Запрос</span><span class="sxs-lookup"><span data-stu-id="e1840-137">Request</span></span>
<span data-ttu-id="e1840-138">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="e1840-138">Here is an example of the request.</span></span>

# <a name="http"></a>[<span data-ttu-id="e1840-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="e1840-139">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "serviceprincipal_checkmembergroups"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/checkMemberGroups
Content-type: application/json
Content-length: 44

{
  "groupIds": [
    "groupIds-value"
  ]
}
```
# <a name="c"></a>[<span data-ttu-id="e1840-140">C#</span><span class="sxs-lookup"><span data-stu-id="e1840-140">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/serviceprincipal-checkmembergroups-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="e1840-141">JavaScript</span><span class="sxs-lookup"><span data-stu-id="e1840-141">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/serviceprincipal-checkmembergroups-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="e1840-142">Objective-C</span><span class="sxs-lookup"><span data-stu-id="e1840-142">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/serviceprincipal-checkmembergroups-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="e1840-143">Ответ</span><span class="sxs-lookup"><span data-stu-id="e1840-143">Response</span></span>
<span data-ttu-id="e1840-p104">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="e1840-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "value": [
    "string-value"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "servicePrincipal: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
