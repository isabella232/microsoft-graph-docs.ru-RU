---
title: 'servicePrincipal: checkMemberGroups'
description: Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье Разрешения.
ms.openlocfilehash: bf16206e9029ddcf687738c3a7db5a0a27a43903
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27074567"
---
# <a name="serviceprincipal-checkmembergroups"></a><span data-ttu-id="c2bbe-104">servicePrincipal: checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="c2bbe-104">servicePrincipal: checkMemberGroups</span></span>

> <span data-ttu-id="c2bbe-105">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="c2bbe-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c2bbe-106">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c2bbe-106">Use of these APIs in production applications is not supported.</span></span>

## <a name="permissions"></a><span data-ttu-id="c2bbe-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="c2bbe-107">Permissions</span></span>
<span data-ttu-id="c2bbe-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c2bbe-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c2bbe-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="c2bbe-110">Permission type</span></span>      | <span data-ttu-id="c2bbe-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="c2bbe-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c2bbe-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c2bbe-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c2bbe-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c2bbe-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c2bbe-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="c2bbe-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c2bbe-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c2bbe-115">Not supported.</span></span>    |
|<span data-ttu-id="c2bbe-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="c2bbe-116">Application</span></span> | <span data-ttu-id="c2bbe-117">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="c2bbe-117">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c2bbe-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="c2bbe-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/checkMemberGroups

```
## <a name="request-headers"></a><span data-ttu-id="c2bbe-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="c2bbe-119">Request headers</span></span>
| <span data-ttu-id="c2bbe-120">Имя</span><span class="sxs-lookup"><span data-stu-id="c2bbe-120">Name</span></span>       | <span data-ttu-id="c2bbe-121">Тип</span><span class="sxs-lookup"><span data-stu-id="c2bbe-121">Type</span></span> | <span data-ttu-id="c2bbe-122">Описание</span><span class="sxs-lookup"><span data-stu-id="c2bbe-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c2bbe-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c2bbe-123">Authorization</span></span>  | <span data-ttu-id="c2bbe-124">string</span><span class="sxs-lookup"><span data-stu-id="c2bbe-124">string</span></span>  | <span data-ttu-id="c2bbe-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="c2bbe-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c2bbe-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="c2bbe-127">Request body</span></span>
<span data-ttu-id="c2bbe-128">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="c2bbe-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c2bbe-129">Параметр</span><span class="sxs-lookup"><span data-stu-id="c2bbe-129">Parameter</span></span>    | <span data-ttu-id="c2bbe-130">Тип</span><span class="sxs-lookup"><span data-stu-id="c2bbe-130">Type</span></span>   |<span data-ttu-id="c2bbe-131">Описание</span><span class="sxs-lookup"><span data-stu-id="c2bbe-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c2bbe-132">groupIds</span><span class="sxs-lookup"><span data-stu-id="c2bbe-132">groupIds</span></span>|<span data-ttu-id="c2bbe-133">String</span><span class="sxs-lookup"><span data-stu-id="c2bbe-133">String</span></span>||

## <a name="response"></a><span data-ttu-id="c2bbe-134">Отклик</span><span class="sxs-lookup"><span data-stu-id="c2bbe-134">Response</span></span>

<span data-ttu-id="c2bbe-135">В случае успеха этот метод возвращает код отклика `200 OK` и объект коллекции String в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="c2bbe-135">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c2bbe-136">Пример</span><span class="sxs-lookup"><span data-stu-id="c2bbe-136">Example</span></span>
<span data-ttu-id="c2bbe-137">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="c2bbe-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c2bbe-138">Запрос</span><span class="sxs-lookup"><span data-stu-id="c2bbe-138">Request</span></span>
<span data-ttu-id="c2bbe-139">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="c2bbe-139">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="c2bbe-140">Ответ</span><span class="sxs-lookup"><span data-stu-id="c2bbe-140">Response</span></span>
<span data-ttu-id="c2bbe-p105">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
</span><span class="sxs-lookup"><span data-stu-id="c2bbe-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
<!-- {
  "type": "#page.annotation",
  "description": "servicePrincipal: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->