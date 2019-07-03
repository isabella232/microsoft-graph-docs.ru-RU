---
title: Добавление владельца группы
description: Добавление пользователя в качестве владельца группы. Владельцы — это группа пользователей, которые не являются администраторами и которым разрешено изменять объект группы.
localization_priority: Priority
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: d2f4f1d8830b154f751db8ef103986d040ce482e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35456388"
---
# <a name="add-group-owner"></a><span data-ttu-id="69206-104">Добавление владельца группы</span><span class="sxs-lookup"><span data-stu-id="69206-104">Add group owner</span></span>
<span data-ttu-id="69206-p102">Добавление пользователя в качестве владельца группы. Владельцы — это группа пользователей, которые не являются администраторами и которым разрешено изменять объект группы.</span><span class="sxs-lookup"><span data-stu-id="69206-p102">Add a user to the group's owners. The owners are a set of non-admin users who are allowed to modify the group object.</span></span>

><span data-ttu-id="69206-107">**Важно!** При обновлении владельцев группы и создании команды для группы может потребоваться до 2 часов для синхронизации владельцев с Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="69206-107">**Important:** If you update the group owners and you created a team for the group, it can take up to 2 hours for the owners to be synchronized with Microsoft Teams.</span></span> <span data-ttu-id="69206-108">Кроме того, если нужно, чтобы владелец мог вносить изменения в команду, например путем создания плана Планировщика, владельца также требуется добавить в качестве участника группы или команды.</span><span class="sxs-lookup"><span data-stu-id="69206-108">Also, if you want the owner to be able to make changes in a team - for example, by creating a Planner plan - the owner also needs to be added as a group/team member.</span></span> 

## <a name="permissions"></a><span data-ttu-id="69206-109">Разрешения</span><span class="sxs-lookup"><span data-stu-id="69206-109">Permissions</span></span>
<span data-ttu-id="69206-p104">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="69206-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="69206-112">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="69206-112">Permission type</span></span>      | <span data-ttu-id="69206-113">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="69206-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="69206-114">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="69206-114">Delegated (work or school account)</span></span> | <span data-ttu-id="69206-115">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="69206-115">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="69206-116">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="69206-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="69206-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="69206-117">Not supported.</span></span>    |
|<span data-ttu-id="69206-118">Приложение</span><span class="sxs-lookup"><span data-stu-id="69206-118">Application</span></span> | <span data-ttu-id="69206-119">Group.ReadWrite.All и User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="69206-119">Group.ReadWrite.All and User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="69206-120">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="69206-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/owners/$ref
```
## <a name="request-headers"></a><span data-ttu-id="69206-121">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="69206-121">Request headers</span></span>
| <span data-ttu-id="69206-122">Имя</span><span class="sxs-lookup"><span data-stu-id="69206-122">Name</span></span>       | <span data-ttu-id="69206-123">Тип</span><span class="sxs-lookup"><span data-stu-id="69206-123">Type</span></span> | <span data-ttu-id="69206-124">Описание</span><span class="sxs-lookup"><span data-stu-id="69206-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="69206-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="69206-125">Authorization</span></span>  | <span data-ttu-id="69206-126">string</span><span class="sxs-lookup"><span data-stu-id="69206-126">string</span></span>  | <span data-ttu-id="69206-p105">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="69206-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="69206-129">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="69206-129">Request body</span></span>
<span data-ttu-id="69206-130">Предоставьте в тексте запроса описание добавляемого объекта [user](../resources/user.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="69206-130">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="69206-131">Отклик</span><span class="sxs-lookup"><span data-stu-id="69206-131">Response</span></span>
<span data-ttu-id="69206-p106">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="69206-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="69206-134">Пример</span><span class="sxs-lookup"><span data-stu-id="69206-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="69206-135">Запрос</span><span class="sxs-lookup"><span data-stu-id="69206-135">Request</span></span>
<span data-ttu-id="69206-136">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="69206-136">The following is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="69206-137">HTTP</span><span class="sxs-lookup"><span data-stu-id="69206-137">--Http</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/owners/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id": "https://graph.microsoft.com/v1.0/users/{id}"
}
```
# <a name="javascripttabjavascript"></a>[<span data-ttu-id="69206-138">JavaScript</span><span class="sxs-lookup"><span data-stu-id="69206-138">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-directoryobject-from-group-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="69206-139">Objective-C</span><span class="sxs-lookup"><span data-stu-id="69206-139">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-directoryobject-from-group-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

<span data-ttu-id="69206-140">Предоставьте в тексте запроса описание добавляемого объекта [user](../resources/user.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="69206-140">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

#### <a name="response"></a><span data-ttu-id="69206-141">Отклик</span><span class="sxs-lookup"><span data-stu-id="69206-141">Response</span></span>
<span data-ttu-id="69206-142">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="69206-142">The following is an example of the response.</span></span>
><span data-ttu-id="69206-143">**Примечание.**  Объект ответа, показанный здесь, может быть сокращен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="69206-143">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="69206-144">При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="69206-144">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create owner",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->

