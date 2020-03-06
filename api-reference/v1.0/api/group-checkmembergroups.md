---
title: 'group: checkMemberGroups'
description: Проверка членства в указанном списке групп. Возвращает из списка те группы, в которых
author: dkershaw10
localization_priority: Priority
ms.prod: groups
doc_type: apiPageType
ms.openlocfilehash: b2ad7dd8e98c88ed428f9a61287027b49f5a73c3
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42517231"
---
# <a name="group-checkmembergroups"></a><span data-ttu-id="f0fc6-104">group: checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="f0fc6-104">group: checkMemberGroups</span></span>

<span data-ttu-id="f0fc6-105">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="f0fc6-105">Namespace: microsoft.graph</span></span>

<span data-ttu-id="f0fc6-p102">Проверка членства в указанном списке групп. Возвращает из списка те группы, в которых указанная группа состоит напрямую или транзитивно.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-p102">Check for membership in the specified list of groups. Returns from the list those groups of which the specified group has a direct or transitive membership.</span></span>

<span data-ttu-id="f0fc6-p103">В одном запросе можно проверять до 20 групп. Эта функция поддерживает Office 365 и другие типы групп, подготовленных в Azure AD. Обратите внимание, что группы Office 365 не могут содержать групп. Следовательно, членство в группе Office 365 всегда непосредственное.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-p103">You can check up to a maximum of 20 groups per request. This function supports Office 365 and other types of groups provisioned in Azure AD. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="f0fc6-112">Разрешения</span><span class="sxs-lookup"><span data-stu-id="f0fc6-112">Permissions</span></span>

<span data-ttu-id="f0fc6-p104">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f0fc6-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="f0fc6-115">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="f0fc6-115">Permission type</span></span>                        | <span data-ttu-id="f0fc6-116">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="f0fc6-116">Permissions (from least to most privileged)</span></span>                                                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------ |
| <span data-ttu-id="f0fc6-117">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="f0fc6-117">Delegated (work or school account)</span></span>     | <span data-ttu-id="f0fc6-118">GroupMember.Read.All, Group.Read.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f0fc6-118">GroupMember.Read.All, Group.Read.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="f0fc6-119">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="f0fc6-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f0fc6-120">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-120">Not supported.</span></span>                                                                              |
| <span data-ttu-id="f0fc6-121">Приложение</span><span class="sxs-lookup"><span data-stu-id="f0fc6-121">Application</span></span>                            | <span data-ttu-id="f0fc6-122">GroupMember.Read.All, Group.Read.All, Directory.Read.All.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-122">GroupMember.Read.All, Group.Read.All, Directory.Read.All.</span></span> <span data-ttu-id="f0fc6-123">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f0fc6-123">Directory.ReadWrite.All</span></span>                               |



## <a name="http-request"></a><span data-ttu-id="f0fc6-124">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="f0fc6-124">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /groups/{id}/checkMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="f0fc6-125">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="f0fc6-125">Request headers</span></span>

| <span data-ttu-id="f0fc6-126">Имя</span><span class="sxs-lookup"><span data-stu-id="f0fc6-126">Name</span></span>          | <span data-ttu-id="f0fc6-127">Тип</span><span class="sxs-lookup"><span data-stu-id="f0fc6-127">Type</span></span>   | <span data-ttu-id="f0fc6-128">Описание</span><span class="sxs-lookup"><span data-stu-id="f0fc6-128">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="f0fc6-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="f0fc6-129">Authorization</span></span> | <span data-ttu-id="f0fc6-130">string</span><span class="sxs-lookup"><span data-stu-id="f0fc6-130">string</span></span> | <span data-ttu-id="f0fc6-p106">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f0fc6-133">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="f0fc6-133">Request body</span></span>

<span data-ttu-id="f0fc6-134">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-134">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f0fc6-135">Параметр</span><span class="sxs-lookup"><span data-stu-id="f0fc6-135">Parameter</span></span> | <span data-ttu-id="f0fc6-136">Тип</span><span class="sxs-lookup"><span data-stu-id="f0fc6-136">Type</span></span>              | <span data-ttu-id="f0fc6-137">Описание</span><span class="sxs-lookup"><span data-stu-id="f0fc6-137">Description</span></span>           |
| :-------- | :---------------- | :-------------------- |
| <span data-ttu-id="f0fc6-138">groupIds</span><span class="sxs-lookup"><span data-stu-id="f0fc6-138">groupIds</span></span>  | <span data-ttu-id="f0fc6-139">Коллекция строк</span><span class="sxs-lookup"><span data-stu-id="f0fc6-139">String collection</span></span> | <span data-ttu-id="f0fc6-140">Массив идентификаторов групп</span><span class="sxs-lookup"><span data-stu-id="f0fc6-140">An array of group ids</span></span> |

## <a name="response"></a><span data-ttu-id="f0fc6-141">Отклик</span><span class="sxs-lookup"><span data-stu-id="f0fc6-141">Response</span></span>

<span data-ttu-id="f0fc6-142">В случае успеха этот метод возвращает код отклика `200 OK` и объект коллекции String в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-142">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f0fc6-143">Пример</span><span class="sxs-lookup"><span data-stu-id="f0fc6-143">Example</span></span>

<span data-ttu-id="f0fc6-144">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-144">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="f0fc6-145">Запрос</span><span class="sxs-lookup"><span data-stu-id="f0fc6-145">Request</span></span>

<span data-ttu-id="f0fc6-146">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-146">Here is an example of the request.</span></span>


# <a name="http"></a>[<span data-ttu-id="f0fc6-147">HTTP</span><span class="sxs-lookup"><span data-stu-id="f0fc6-147">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "group_checkmembergroups"
}-->

```http
POST https://graph.microsoft.com/v1.0/groups/{id}/checkMemberGroups
Content-type: application/json
Content-length: 44

{
  "groupIds": [
    "groupIds-value"
  ]
}
```
# <a name="c"></a>[<span data-ttu-id="f0fc6-148">C#</span><span class="sxs-lookup"><span data-stu-id="f0fc6-148">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/group-checkmembergroups-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[<span data-ttu-id="f0fc6-149">JavaScript</span><span class="sxs-lookup"><span data-stu-id="f0fc6-149">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/group-checkmembergroups-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[<span data-ttu-id="f0fc6-150">Objective-C</span><span class="sxs-lookup"><span data-stu-id="f0fc6-150">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/group-checkmembergroups-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[<span data-ttu-id="f0fc6-151">Java</span><span class="sxs-lookup"><span data-stu-id="f0fc6-151">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/group-checkmembergroups-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="f0fc6-152">Отклик</span><span class="sxs-lookup"><span data-stu-id="f0fc6-152">Response</span></span>

<span data-ttu-id="f0fc6-p107">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="f0fc6-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
  "description": "group: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
