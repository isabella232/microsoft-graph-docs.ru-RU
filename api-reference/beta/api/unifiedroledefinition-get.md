---
title: Получение Унифиедроледефинитион
description: Получение свойств и связей объекта Унифиедроледефинитион.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: f55e4f46b758db9108d675ef36e934852d708997
ms.sourcegitcommit: f50b1feff72182d1e19bfa346304beaf29558b68
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2019
ms.locfileid: "36461660"
---
# <a name="get-unifiedroledefinition"></a><span data-ttu-id="d08a8-103">Получение Унифиедроледефинитион</span><span class="sxs-lookup"><span data-stu-id="d08a8-103">Get unifiedRoleDefinition</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="d08a8-104">Получение свойств и связей объекта [унифиедроледефинитион](../resources/unifiedRoleDefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="d08a8-104">Retrieve the properties and relationships of a [unifiedRoleDefinition](../resources/unifiedRoleDefinition.md) object.</span></span> <span data-ttu-id="d08a8-105">В настоящее время "каталог" является единственным поддерживаемым приложением RBAC.</span><span class="sxs-lookup"><span data-stu-id="d08a8-105">Currently "directory" is the only RBAC application supported.</span></span>

## <a name="permissions"></a><span data-ttu-id="d08a8-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="d08a8-106">Permissions</span></span>

<span data-ttu-id="d08a8-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d08a8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d08a8-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="d08a8-109">Permission type</span></span>      | <span data-ttu-id="d08a8-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="d08a8-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d08a8-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d08a8-111">Delegated (work or school account)</span></span> | <span data-ttu-id="d08a8-112">Ролеманажемент. Read. Directory, Directory. Read. ALL, Ролеманажемент. ReadWrite. Directory, Directory. ReadWrite. ALL, Directory. AccessAsUser. ALL</span><span class="sxs-lookup"><span data-stu-id="d08a8-112">RoleManagement.Read.Directory, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="d08a8-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="d08a8-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d08a8-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d08a8-114">Not supported.</span></span>    |
|<span data-ttu-id="d08a8-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="d08a8-115">Application</span></span> | <span data-ttu-id="d08a8-116">Ролеманажемент. Read. Directory, Directory. Read. ALL, Ролеманажемент. ReadWrite. Directory, Directory. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="d08a8-116">RoleManagement.Read.Directory, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d08a8-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="d08a8-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /roleManagement/{rbacApplication}/roleDefinitions/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="d08a8-118">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="d08a8-118">Optional query parameters</span></span>

<span data-ttu-id="d08a8-119">Этот метод поддерживает параметры запросов OData для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="d08a8-119">This method supports OData query parameters to help customize the response.</span></span> <span data-ttu-id="d08a8-120">Общие сведения можно найти в разделе [Параметры запроса OData](/graph/query-parameters).</span><span class="sxs-lookup"><span data-stu-id="d08a8-120">For general information, see [OData query parameters](/graph/query-parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="d08a8-121">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="d08a8-121">Request headers</span></span>

| <span data-ttu-id="d08a8-122">Имя</span><span class="sxs-lookup"><span data-stu-id="d08a8-122">Name</span></span>      |<span data-ttu-id="d08a8-123">Описание</span><span class="sxs-lookup"><span data-stu-id="d08a8-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d08a8-124">Авторизация</span><span class="sxs-lookup"><span data-stu-id="d08a8-124">Authorization</span></span> | <span data-ttu-id="d08a8-125">Bearer {token}</span><span class="sxs-lookup"><span data-stu-id="d08a8-125">Bearer {token}</span></span> |

## <a name="request-body"></a><span data-ttu-id="d08a8-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="d08a8-126">Request body</span></span>

<span data-ttu-id="d08a8-127">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="d08a8-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d08a8-128">Отклик</span><span class="sxs-lookup"><span data-stu-id="d08a8-128">Response</span></span>

<span data-ttu-id="d08a8-129">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и запрошенный объект [унифиедроледефинитион](../resources/unifiedroledefinition.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="d08a8-129">If successful, this method returns a `200 OK` response code and the requested [unifiedRoleDefinition](../resources/unifiedroledefinition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d08a8-130">Пример</span><span class="sxs-lookup"><span data-stu-id="d08a8-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="d08a8-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="d08a8-131">Request</span></span>

<span data-ttu-id="d08a8-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="d08a8-132">The following is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="d08a8-133">HTTP</span><span class="sxs-lookup"><span data-stu-id="d08a8-133">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_unifiedroledefinition"
}-->

```http
GET https://graph.microsoft.com/beta/roleManagement/directory/roleDefinitions/f189965f-f560-4c59-9101-933d4c87a91a
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="d08a8-134">C#</span><span class="sxs-lookup"><span data-stu-id="d08a8-134">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-unifiedroledefinition-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="d08a8-135">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d08a8-135">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-unifiedroledefinition-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="d08a8-136">Цель — C</span><span class="sxs-lookup"><span data-stu-id="d08a8-136">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-unifiedroledefinition-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="d08a8-137">Отклик</span><span class="sxs-lookup"><span data-stu-id="d08a8-137">Response</span></span>

<span data-ttu-id="d08a8-138">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="d08a8-138">The following is an example of the response.</span></span>

> <span data-ttu-id="d08a8-p104">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="d08a8-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.unifiedRoleDefinition"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json


{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#roleManagement/directory/roleDefinitions/$entity",
    "id": "f189965f-f560-4c59-9101-933d4c87a91a",
    "description": "Allows reading Application Registrations",
    "displayName": "Application Registration Reader",
    "isBuiltIn": false,
    "isEnabled": true,
    "resourceScopes": [
        "/"
    ],
    "templateId": "429c3819-053d-4250-9926-4c7dcb18ae17",
    "version": null,
    "rolePermissions": [
        {
            "allowedResourceActions": [
                "microsoft.directory/applications/allProperties/read"
            ],
            "condition": null
        }
    ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get unifiedRoleDefinition",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->