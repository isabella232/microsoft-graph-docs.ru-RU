---
title: Восстановление удаленного элемента
description: 'Восстановление недавно удаленного элемента из контейнера для удаленных элементов. '
author: davidmu1
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: ce665b06da098661de1ba27a9ea1648470e15ae0
ms.sourcegitcommit: 6720736406f21e40914b27ba28387adedf97fa56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2019
ms.locfileid: "35638974"
---
# <a name="restore-deleted-item"></a><span data-ttu-id="b728d-103">Восстановление удаленного элемента</span><span class="sxs-lookup"><span data-stu-id="b728d-103">Restore deleted item</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="b728d-104">Восстановление недавно удаленного элемента из контейнера для [удаленных элементов](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="b728d-104">Restores a recently deleted item from [deleted items](../resources/directory.md).</span></span> 

<span data-ttu-id="b728d-105">В настоящее время хранение удаленных элементов поддерживается только для ресурсов [group](../resources/group.md) и [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="b728d-105">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span> <span data-ttu-id="b728d-106">Вы можете полностью восстановить случайно удаленный элемент.</span><span class="sxs-lookup"><span data-stu-id="b728d-106">If an item was accidentally deleted, you can fully restore the item.</span></span>

<span data-ttu-id="b728d-107">Удаленный элемент можно восстановить в течение 30 дней.</span><span class="sxs-lookup"><span data-stu-id="b728d-107">A recently deleted item will remain available for up to 30 days.</span></span> <span data-ttu-id="b728d-108">Через 30 дней элемент удаляется без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="b728d-108">After 30 days, the item is permanently deleted.</span></span>

## <a name="permissions"></a><span data-ttu-id="b728d-109">Разрешения</span><span class="sxs-lookup"><span data-stu-id="b728d-109">Permissions</span></span>
<span data-ttu-id="b728d-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b728d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

* <span data-ttu-id="b728d-112">Для пользователей: User. ReadWrite. ALL, Directory. AccessAsUser. ALL</span><span class="sxs-lookup"><span data-stu-id="b728d-112">For users: User.ReadWrite.All, Directory.AccessAsUser.All</span></span>
* <span data-ttu-id="b728d-113">Для групп: Group. ReadWrite. ALL, Directory. AccessAsUser. ALL</span><span class="sxs-lookup"><span data-stu-id="b728d-113">For groups: Group.ReadWrite.All, Directory.AccessAsUser.All</span></span>

## <a name="http-request"></a><span data-ttu-id="b728d-114">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="b728d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /directory/deleteditems/{id}/restore
```

## <a name="request-headers"></a><span data-ttu-id="b728d-115">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="b728d-115">Request headers</span></span>
| <span data-ttu-id="b728d-116">Имя</span><span class="sxs-lookup"><span data-stu-id="b728d-116">Name</span></span>       | <span data-ttu-id="b728d-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b728d-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b728d-118">Авторизация</span><span class="sxs-lookup"><span data-stu-id="b728d-118">Authorization</span></span>  | <span data-ttu-id="b728d-119">&lt;&gt; *Необходим* маркер носителя</span><span class="sxs-lookup"><span data-stu-id="b728d-119">Bearer &lt;token&gt; *Required*</span></span>|
| <span data-ttu-id="b728d-120">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b728d-120">Content-type</span></span> | <span data-ttu-id="b728d-121">application/json</span><span class="sxs-lookup"><span data-stu-id="b728d-121">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="b728d-122">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="b728d-122">Request body</span></span>
<span data-ttu-id="b728d-123">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="b728d-123">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b728d-124">Отклик</span><span class="sxs-lookup"><span data-stu-id="b728d-124">Response</span></span>

<span data-ttu-id="b728d-125">В случае успеха этот метод возвращает код отклика `200 OK` и объект [directoryObject](../resources/directoryobject.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="b728d-125">If successful, this method returns a `200 OK` response code and a [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b728d-126">Пример</span><span class="sxs-lookup"><span data-stu-id="b728d-126">Example</span></span>
### <a name="request"></a><span data-ttu-id="b728d-127">Запрос</span><span class="sxs-lookup"><span data-stu-id="b728d-127">Request</span></span>


# <a name="httptabhttp"></a>[<span data-ttu-id="b728d-128">HTTP</span><span class="sxs-lookup"><span data-stu-id="b728d-128">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_directory"
}-->
```http
POST https://graph.microsoft.com/beta/directory/deleteditems/46cc6179-19d0-473e-97ad-6ff84347bbbb/restore
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="b728d-129">C#</span><span class="sxs-lookup"><span data-stu-id="b728d-129">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-directoryobject-from-directory-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="b728d-130">Javascript</span><span class="sxs-lookup"><span data-stu-id="b728d-130">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-directoryobject-from-directory-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="b728d-131">Цель — C</span><span class="sxs-lookup"><span data-stu-id="b728d-131">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-directoryobject-from-directory-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### <a name="response"></a><span data-ttu-id="b728d-132">Отклик</span><span class="sxs-lookup"><span data-stu-id="b728d-132">Response</span></span>
<span data-ttu-id="b728d-p104">Примечание. Представленный здесь объект отклика может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="b728d-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#directoryObjects/$entity",
  "@odata.type":"#microsoft.graph.group",
  "id":"46cc6179-19d0-473e-97ad-6ff84347bbbb",
  "displayName":"SampleGroup",
  "groupTypes":["Unified"],
  "mail":"example@contoso.com",
  "mailEnabled":true,
  "mailNickname":"Example",
  "securityEnabled":false,
  "visibility":"Public"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create deletedItem",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
