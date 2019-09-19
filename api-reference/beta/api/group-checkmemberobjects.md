---
title: 'Группа: Чеккмемберобжектс'
description: Проверка членства в списке групп, ролей каталогов или административных единиц для указанного объекта Group.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 45842a31bb4e7a7b2ec3e5405aa17c4cf6a5a53d
ms.sourcegitcommit: 997fbfe36b518e0a8c230ae2e62666bb5c829e7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/19/2019
ms.locfileid: "37041820"
---
# <a name="group-checkmemberobjects"></a><span data-ttu-id="7a0a3-103">Группа: Чеккмемберобжектс</span><span class="sxs-lookup"><span data-stu-id="7a0a3-103">group: checkMemberObjects</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="7a0a3-104">Проверка членства в списке групп или административных единиц для указанной группы.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-104">Check for membership in a list of groups or administrative units for the specified group.</span></span> <span data-ttu-id="7a0a3-105">Этот метод является транзитивным.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-105">This method is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="7a0a3-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="7a0a3-106">Permissions</span></span>

<span data-ttu-id="7a0a3-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7a0a3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7a0a3-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="7a0a3-109">Permission type</span></span>                        | <span data-ttu-id="7a0a3-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="7a0a3-110">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="7a0a3-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7a0a3-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="7a0a3-112">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7a0a3-112">Group.Read.All, Group.ReadWrite.All</span></span><br><span data-ttu-id="7a0a3-113">С</span><span class="sxs-lookup"><span data-stu-id="7a0a3-113">And:</span></span><br><ul><li><span data-ttu-id="7a0a3-114">При проверке принадлежности к административным единицам: AdministrativeUnit. Read. ALL, AdministrativeUnit. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="7a0a3-114">If checking for membership in administrative units: AdministrativeUnit.Read.All, AdministrativeUnit.ReadWrite.All</span></span></li></ul><br><span data-ttu-id="7a0a3-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7a0a3-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="7a0a3-116">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="7a0a3-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7a0a3-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-117">Not supported.</span></span> |
| <span data-ttu-id="7a0a3-118">Для приложений</span><span class="sxs-lookup"><span data-stu-id="7a0a3-118">Application</span></span>                            | <span data-ttu-id="7a0a3-119">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7a0a3-119">Group.Read.All, Group.ReadWrite.All</span></span><br><span data-ttu-id="7a0a3-120">С</span><span class="sxs-lookup"><span data-stu-id="7a0a3-120">And:</span></span><br><ul><li><span data-ttu-id="7a0a3-121">При проверке принадлежности к административным единицам: AdministrativeUnit. Read. ALL, AdministrativeUnit. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="7a0a3-121">If checking for membership in administrative units: AdministrativeUnit.Read.All, AdministrativeUnit.ReadWrite.All</span></span></ul></li><br><span data-ttu-id="7a0a3-122">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7a0a3-122">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7a0a3-123">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="7a0a3-123">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /groups/{id}/checkMemberObjects
```

## <a name="request-headers"></a><span data-ttu-id="7a0a3-124">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="7a0a3-124">Request headers</span></span>

| <span data-ttu-id="7a0a3-125">Имя</span><span class="sxs-lookup"><span data-stu-id="7a0a3-125">Name</span></span>          | <span data-ttu-id="7a0a3-126">Описание</span><span class="sxs-lookup"><span data-stu-id="7a0a3-126">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="7a0a3-127">Авторизация</span><span class="sxs-lookup"><span data-stu-id="7a0a3-127">Authorization</span></span> | <span data-ttu-id="7a0a3-128">Bearer {token}</span><span class="sxs-lookup"><span data-stu-id="7a0a3-128">Bearer {token}</span></span> |
| <span data-ttu-id="7a0a3-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7a0a3-129">Content-Type</span></span>  | <span data-ttu-id="7a0a3-130">application/json</span><span class="sxs-lookup"><span data-stu-id="7a0a3-130">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="7a0a3-131">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="7a0a3-131">Request body</span></span>

<span data-ttu-id="7a0a3-132">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7a0a3-133">Параметр</span><span class="sxs-lookup"><span data-stu-id="7a0a3-133">Parameter</span></span>    | <span data-ttu-id="7a0a3-134">Тип</span><span class="sxs-lookup"><span data-stu-id="7a0a3-134">Type</span></span>        | <span data-ttu-id="7a0a3-135">Описание</span><span class="sxs-lookup"><span data-stu-id="7a0a3-135">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="7a0a3-136">ids</span><span class="sxs-lookup"><span data-stu-id="7a0a3-136">ids</span></span>|<span data-ttu-id="7a0a3-137">Коллекция String</span><span class="sxs-lookup"><span data-stu-id="7a0a3-137">String collection</span></span>| <span data-ttu-id="7a0a3-138">Коллекция, содержащая идентификаторы объектов групп, ролей каталогов, административных единиц или идентификаторов Ролетемплате ролей каталогов, в которых проверяется членство.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-138">A collection that contains the object IDs of the groups, directory roles, administrative units, or roleTemplate IDs of directory roles, in which to check membership.</span></span> <span data-ttu-id="7a0a3-139">Можно указать до 20 объектов.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-139">Up to 20 objects may be specified.</span></span> |

## <a name="response"></a><span data-ttu-id="7a0a3-140">Отклик</span><span class="sxs-lookup"><span data-stu-id="7a0a3-140">Response</span></span>

<span data-ttu-id="7a0a3-141">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и объект коллекции String в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-141">If successful, this method returns a `200 OK` response code and a String collection object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="7a0a3-142">Примеры</span><span class="sxs-lookup"><span data-stu-id="7a0a3-142">Examples</span></span>

<span data-ttu-id="7a0a3-143">В приведенном ниже примере показано, как вызывать этот API.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-143">The following example shows how to call this API.</span></span>

### <a name="request"></a><span data-ttu-id="7a0a3-144">Запрос</span><span class="sxs-lookup"><span data-stu-id="7a0a3-144">Request</span></span>

<span data-ttu-id="7a0a3-145">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-145">The following is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="7a0a3-146">HTTP</span><span class="sxs-lookup"><span data-stu-id="7a0a3-146">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "group_checkmemberobjects"
}-->

```http
POST https://graph.microsoft.com/beta/groups/{id}/checkMemberObjects
Content-type: application/json

{
  "ids": [
    "80a963dd-84af-4eb8-b2a6-781e444d4fb0",
    "62e90394-69f5-4237-9190-012177145e10",
    "86a64f51-3a64-4cc6-a8c8-6b8f000c0f52",
    "ac38546e-ddf3-437a-ac5c-27a94cd7a0f1"
  ]
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="7a0a3-147">C#</span><span class="sxs-lookup"><span data-stu-id="7a0a3-147">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/group-checkmemberobjects-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="7a0a3-148">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7a0a3-148">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/group-checkmemberobjects-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="7a0a3-149">Цель — C</span><span class="sxs-lookup"><span data-stu-id="7a0a3-149">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/group-checkmemberobjects-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="7a0a3-150">Отклик</span><span class="sxs-lookup"><span data-stu-id="7a0a3-150">Response</span></span>

<span data-ttu-id="7a0a3-151">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-151">The following is an example of the response.</span></span> 

> <span data-ttu-id="7a0a3-p104">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "String",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    "80a963dd-84af-4eb8-b2a6-781e444d4fb0", 
    "62e90394-69f5-4237-9190-012177145e10"
  ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: checkMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->