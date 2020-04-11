---
title: Тип ресурса Акцесспаккаже
description: Пакет Access определяет коллекции ролей ресурсов и политики, которые могут получить доступ к этим ресурсам для одного или нескольких пользователей.
localization_priority: Normal
author: markwahl-msft
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: d49ddfcc0db9b55701f0b84a223efcec85aa8dfe
ms.sourcegitcommit: 9a6ce4ddf75beead19b7c35a1949cf4d105b9b29
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/11/2020
ms.locfileid: "43228067"
---
# <a name="accesspackage-resource-type"></a><span data-ttu-id="6cc25-103">Тип ресурса Акцесспаккаже</span><span class="sxs-lookup"><span data-stu-id="6cc25-103">accessPackage resource type</span></span>

<span data-ttu-id="6cc25-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="6cc25-104">Namespace: microsoft.graph</span></span>



<span data-ttu-id="6cc25-105">В [управлении службой управления правами Azure AD](entitlementmanagement-root.md)пакет Access определяет коллекции ролей ресурсов и политики того, как один или несколько пользователей могут получить доступ к этим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="6cc25-105">In [Azure AD entitlement management](entitlementmanagement-root.md), an access package defines the collections of resource roles and the policies for how one or more users can get access to those resources.</span></span>  
<span data-ttu-id="6cc25-106">Каждый пакет Access ссылается на один каталог пакетов доступа и содержит ссылки на ресурсы из этого каталога с помощью областей ролей, определяющих доступ к пакету.</span><span class="sxs-lookup"><span data-stu-id="6cc25-106">Each access package is referenced by a single access package catalog, and has links to the resources from that catalog via the resource-specific role scopes that define the access the package provides.</span></span>  <span data-ttu-id="6cc25-107">Пакет Access также содержит ссылки на политики назначения пакетов Access, каждый из которых определяет, кто может запрашивать или назначать назначение пакета Access.</span><span class="sxs-lookup"><span data-stu-id="6cc25-107">An access package also links to the access package assignment policies, each of which define who can request or be assigned an access package assignment.</span></span>

<span data-ttu-id="6cc25-108">Чтобы назначить пользователя пакету Access, [Создайте акцесспаккажеассигнментрекуест](../api/accesspackageassignmentrequest-post.md) , ссылающийся на политику назначения пакетов доступа и пакетов Access.</span><span class="sxs-lookup"><span data-stu-id="6cc25-108">To assign a user to an access package, [create an accessPackageAssignmentRequest](../api/accesspackageassignmentrequest-post.md) that references the access package and access package assignment policy.</span></span>

## <a name="methods"></a><span data-ttu-id="6cc25-109">Методы</span><span class="sxs-lookup"><span data-stu-id="6cc25-109">Methods</span></span>

| <span data-ttu-id="6cc25-110">Метод</span><span class="sxs-lookup"><span data-stu-id="6cc25-110">Method</span></span>       | <span data-ttu-id="6cc25-111">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="6cc25-111">Return Type</span></span> | <span data-ttu-id="6cc25-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6cc25-112">Description</span></span> |
|:-------------|:------------|:------------|
| [<span data-ttu-id="6cc25-113">Список Акцесспаккажес</span><span class="sxs-lookup"><span data-stu-id="6cc25-113">List accessPackages</span></span>](../api/accesspackage-list.md) | <span data-ttu-id="6cc25-114">Коллекция [акцесспаккаже](accesspackage.md)</span><span class="sxs-lookup"><span data-stu-id="6cc25-114">[accessPackage](accesspackage.md) collection</span></span> | <span data-ttu-id="6cc25-115">Получение списка объектов **акцесспаккаже** .</span><span class="sxs-lookup"><span data-stu-id="6cc25-115">Retrieve a list of **accesspackage** objects.</span></span> |
| [<span data-ttu-id="6cc25-116">Создание Акцесспаккаже</span><span class="sxs-lookup"><span data-stu-id="6cc25-116">Create accessPackage</span></span>](../api/accesspackage-post.md) | [<span data-ttu-id="6cc25-117">акцесспаккаже</span><span class="sxs-lookup"><span data-stu-id="6cc25-117">accessPackage</span></span>](accesspackage.md) | <span data-ttu-id="6cc25-118">Создание нового объекта **акцесспаккаже** .</span><span class="sxs-lookup"><span data-stu-id="6cc25-118">Create a new **accesspackage** object.</span></span> |
| [<span data-ttu-id="6cc25-119">Получение Акцесспаккаже</span><span class="sxs-lookup"><span data-stu-id="6cc25-119">Get accessPackage</span></span>](../api/accesspackage-get.md) | [<span data-ttu-id="6cc25-120">акцесспаккаже</span><span class="sxs-lookup"><span data-stu-id="6cc25-120">accessPackage</span></span>](accesspackage.md) | <span data-ttu-id="6cc25-121">Чтение свойств и связей объекта **акцесспаккаже** .</span><span class="sxs-lookup"><span data-stu-id="6cc25-121">Read properties and relationships of an **accesspackage** object.</span></span> |
| [<span data-ttu-id="6cc25-122">Удаление Акцесспаккаже</span><span class="sxs-lookup"><span data-stu-id="6cc25-122">Delete accessPackage</span></span>](../api/accesspackage-delete.md) |<span data-ttu-id="6cc25-123">Нет</span><span class="sxs-lookup"><span data-stu-id="6cc25-123">None</span></span> | <span data-ttu-id="6cc25-124">Удаление **акцесспаккаже**.</span><span class="sxs-lookup"><span data-stu-id="6cc25-124">Delete an **accesspackage**.</span></span> |
| [<span data-ttu-id="6cc25-125">Список Акцесспаккажересаурцеролескопес</span><span class="sxs-lookup"><span data-stu-id="6cc25-125">List accessPackageResourceRoleScopes</span></span>](../api/accesspackage-list-accesspackageresourcerolescopes.md) | <span data-ttu-id="6cc25-126">Коллекция [акцесспаккажересаурцеролескопе](accesspackageresourcerolescope.md)</span><span class="sxs-lookup"><span data-stu-id="6cc25-126">[accessPackageResourceRoleScope](accesspackageresourcerolescope.md) collection</span></span> | <span data-ttu-id="6cc25-127">Получение списка объектов **акцесспаккажересаурцеролескопе** для этого пакета Access.</span><span class="sxs-lookup"><span data-stu-id="6cc25-127">Retrieve a list of **accessPackageResourceRoleScope** objects for this access package.</span></span> |
| [<span data-ttu-id="6cc25-128">Создание Акцесспаккажересаурцеролескопе</span><span class="sxs-lookup"><span data-stu-id="6cc25-128">Create accessPackageResourceRoleScope</span></span>](../api/accesspackage-post-accesspackageresourcerolescopes.md) |<span data-ttu-id="6cc25-129">Нет</span><span class="sxs-lookup"><span data-stu-id="6cc25-129">None</span></span> | <span data-ttu-id="6cc25-130">Создайте новый объект **акцесспаккажересаурцеролескопе** для этого пакета Access.</span><span class="sxs-lookup"><span data-stu-id="6cc25-130">Create a new **accessPackageResourceRoleScope** object for this access package.</span></span> |

## <a name="properties"></a><span data-ttu-id="6cc25-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="6cc25-131">Properties</span></span>

| <span data-ttu-id="6cc25-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="6cc25-132">Property</span></span>     | <span data-ttu-id="6cc25-133">Тип</span><span class="sxs-lookup"><span data-stu-id="6cc25-133">Type</span></span>        | <span data-ttu-id="6cc25-134">Описание</span><span class="sxs-lookup"><span data-stu-id="6cc25-134">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="6cc25-135">каталогид</span><span class="sxs-lookup"><span data-stu-id="6cc25-135">catalogId</span></span>|<span data-ttu-id="6cc25-136">String</span><span class="sxs-lookup"><span data-stu-id="6cc25-136">String</span></span>|<span data-ttu-id="6cc25-137">Идентификатор каталога пакетов доступа, на который ссылается этот пакет Access.</span><span class="sxs-lookup"><span data-stu-id="6cc25-137">ID of the access package catalog referencing this access package.</span></span> <span data-ttu-id="6cc25-138">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6cc25-138">Read-only.</span></span>|
|<span data-ttu-id="6cc25-139">createdBy</span><span class="sxs-lookup"><span data-stu-id="6cc25-139">createdBy</span></span>|<span data-ttu-id="6cc25-140">String</span><span class="sxs-lookup"><span data-stu-id="6cc25-140">String</span></span>|<span data-ttu-id="6cc25-141">Имя участника-пользователя или идентификатор субъекта, создавшего этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="6cc25-141">UPN of the user or identity of the subject who created this resource.</span></span> <span data-ttu-id="6cc25-142">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6cc25-142">Read-only.</span></span>|
|<span data-ttu-id="6cc25-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="6cc25-143">createdDateTime</span></span>|<span data-ttu-id="6cc25-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6cc25-144">DateTimeOffset</span></span>|<span data-ttu-id="6cc25-145">Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC).</span><span class="sxs-lookup"><span data-stu-id="6cc25-145">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="6cc25-146">Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="6cc25-146">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span> <span data-ttu-id="6cc25-147">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6cc25-147">Read-only.</span></span>|
|<span data-ttu-id="6cc25-148">description</span><span class="sxs-lookup"><span data-stu-id="6cc25-148">description</span></span>|<span data-ttu-id="6cc25-149">String</span><span class="sxs-lookup"><span data-stu-id="6cc25-149">String</span></span>|<span data-ttu-id="6cc25-150">Описание пакета Access.</span><span class="sxs-lookup"><span data-stu-id="6cc25-150">The description of the access package.</span></span>|
|<span data-ttu-id="6cc25-151">displayName</span><span class="sxs-lookup"><span data-stu-id="6cc25-151">displayName</span></span>|<span data-ttu-id="6cc25-152">Строка</span><span class="sxs-lookup"><span data-stu-id="6cc25-152">String</span></span>|<span data-ttu-id="6cc25-153">Отображаемое имя пакета Access.</span><span class="sxs-lookup"><span data-stu-id="6cc25-153">The display name of the access package.</span></span>|
|<span data-ttu-id="6cc25-154">id</span><span class="sxs-lookup"><span data-stu-id="6cc25-154">id</span></span>|<span data-ttu-id="6cc25-155">String</span><span class="sxs-lookup"><span data-stu-id="6cc25-155">String</span></span>| <span data-ttu-id="6cc25-156">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6cc25-156">Read-only.</span></span>|
|<span data-ttu-id="6cc25-157">Скрытый</span><span class="sxs-lookup"><span data-stu-id="6cc25-157">isHidden</span></span>|<span data-ttu-id="6cc25-158">Логический</span><span class="sxs-lookup"><span data-stu-id="6cc25-158">Boolean</span></span>|<span data-ttu-id="6cc25-159">Указывает, является ли пакет доступа скрытым от запрашивающего.</span><span class="sxs-lookup"><span data-stu-id="6cc25-159">Whether the access package is hidden from the requestor.</span></span>|
|<span data-ttu-id="6cc25-160">исролескопесвисибле</span><span class="sxs-lookup"><span data-stu-id="6cc25-160">isRoleScopesVisible</span></span>|<span data-ttu-id="6cc25-161">Логический</span><span class="sxs-lookup"><span data-stu-id="6cc25-161">Boolean</span></span>|<span data-ttu-id="6cc25-162">Указывает, видимы ли области ролей.</span><span class="sxs-lookup"><span data-stu-id="6cc25-162">Indicates whether role scopes are visible.</span></span>|
|<span data-ttu-id="6cc25-163">модифиедби</span><span class="sxs-lookup"><span data-stu-id="6cc25-163">modifiedBy</span></span>|<span data-ttu-id="6cc25-164">String</span><span class="sxs-lookup"><span data-stu-id="6cc25-164">String</span></span>|<span data-ttu-id="6cc25-165">Имя участника-пользователя, который последним изменил этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="6cc25-165">The UPN of the user who last modified this resource.</span></span> <span data-ttu-id="6cc25-166">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6cc25-166">Read-only.</span></span>|
|<span data-ttu-id="6cc25-167">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="6cc25-167">modifiedDateTime</span></span>|<span data-ttu-id="6cc25-168">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6cc25-168">DateTimeOffset</span></span>|<span data-ttu-id="6cc25-169">Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC).</span><span class="sxs-lookup"><span data-stu-id="6cc25-169">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="6cc25-170">Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="6cc25-170">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span> <span data-ttu-id="6cc25-171">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6cc25-171">Read-only.</span></span> |

## <a name="relationships"></a><span data-ttu-id="6cc25-172">Отношения</span><span class="sxs-lookup"><span data-stu-id="6cc25-172">Relationships</span></span>

| <span data-ttu-id="6cc25-173">Связь</span><span class="sxs-lookup"><span data-stu-id="6cc25-173">Relationship</span></span> | <span data-ttu-id="6cc25-174">Тип</span><span class="sxs-lookup"><span data-stu-id="6cc25-174">Type</span></span>        | <span data-ttu-id="6cc25-175">Описание</span><span class="sxs-lookup"><span data-stu-id="6cc25-175">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="6cc25-176">акцесспаккажеассигнментполиЦиес</span><span class="sxs-lookup"><span data-stu-id="6cc25-176">accessPackageAssignmentPolicies</span></span>|<span data-ttu-id="6cc25-177">Коллекция [акцесспаккажеассигнментполици](accesspackageassignmentpolicy.md)</span><span class="sxs-lookup"><span data-stu-id="6cc25-177">[accessPackageAssignmentPolicy](accesspackageassignmentpolicy.md) collection</span></span>| <span data-ttu-id="6cc25-178">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6cc25-178">Read-only.</span></span> <span data-ttu-id="6cc25-179">Допускается значение null.</span><span class="sxs-lookup"><span data-stu-id="6cc25-179">Nullable.</span></span>|
|<span data-ttu-id="6cc25-180">акцесспаккажекаталог</span><span class="sxs-lookup"><span data-stu-id="6cc25-180">accessPackageCatalog</span></span>|[<span data-ttu-id="6cc25-181">акцесспаккажекаталог</span><span class="sxs-lookup"><span data-stu-id="6cc25-181">accessPackageCatalog</span></span>](accesspackagecatalog.md)| <span data-ttu-id="6cc25-182">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6cc25-182">Read-only.</span></span> <span data-ttu-id="6cc25-183">Допускается значение null.</span><span class="sxs-lookup"><span data-stu-id="6cc25-183">Nullable.</span></span>|
|<span data-ttu-id="6cc25-184">акцесспаккажересаурцеролескопес</span><span class="sxs-lookup"><span data-stu-id="6cc25-184">accessPackageResourceRoleScopes</span></span>|<span data-ttu-id="6cc25-185">Коллекция [акцесспаккажересаурцеролескопе](accesspackageresourcerolescope.md)</span><span class="sxs-lookup"><span data-stu-id="6cc25-185">[accessPackageResourceRoleScope](accesspackageresourcerolescope.md) collection</span></span>| <span data-ttu-id="6cc25-186">Допускается значение null.</span><span class="sxs-lookup"><span data-stu-id="6cc25-186">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6cc25-187">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="6cc25-187">JSON representation</span></span>

<span data-ttu-id="6cc25-188">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="6cc25-188">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.accessPackage",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
    "id":"360fa7de-90be-48dc-a2ce-fc40094a93dd",
    "description":"Sample access package",
    "displayName":"Access package for testing",
    "isHidden":false,
    "catalogId":"662d99e7-6ceb-4c21-9cb4-9b0bbfdefccc",
    "isRoleScopesVisible":false,
    "createdDateTime":"2019-01-27T18:19:50.74Z",
    "modifiedDateTime":"2019-01-27T18:19:50.74Z",
    "createdBy":"TestGA@example.com",
    "modifiedBy":"TestGA@example.com"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "accessPackage resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
