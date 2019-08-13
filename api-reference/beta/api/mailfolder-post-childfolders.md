---
title: Создание объекта MailFolder
description: Используйте этот API для создания нового дочернего элемента mailFolder.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: 7690d79c8745fc1b0ed54f7053af89c0c5d3d4fd
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "36347075"
---
# <a name="create-mailfolder"></a><span data-ttu-id="5efd1-103">Создание объекта MailFolder</span><span class="sxs-lookup"><span data-stu-id="5efd1-103">Create mailFolder</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="5efd1-104">Используйте этот API для создания нового дочернего элемента [mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="5efd1-104">Use this API to create a new child [mailFolder](../resources/mailfolder.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="5efd1-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="5efd1-105">Permissions</span></span>

<span data-ttu-id="5efd1-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5efd1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="5efd1-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="5efd1-108">Permission type</span></span> | <span data-ttu-id="5efd1-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="5efd1-109">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="5efd1-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="5efd1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="5efd1-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5efd1-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="5efd1-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="5efd1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5efd1-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5efd1-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="5efd1-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="5efd1-114">Application</span></span> | <span data-ttu-id="5efd1-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5efd1-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="5efd1-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="5efd1-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/mailFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```

<span data-ttu-id="5efd1-117">Укажите родительскую папку в URL-адресе запроса как идентификатор папки или известное имя папки.</span><span class="sxs-lookup"><span data-stu-id="5efd1-117">Specify the parent folder in the query URL as a folder ID, or a well-known folder name.</span></span> <span data-ttu-id="5efd1-118">Список поддерживаемых известных имен см. в статье [Тип ресурса mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="5efd1-118">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>

## <a name="request-headers"></a><span data-ttu-id="5efd1-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="5efd1-119">Request headers</span></span>

| <span data-ttu-id="5efd1-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5efd1-120">Header</span></span> | <span data-ttu-id="5efd1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5efd1-121">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="5efd1-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="5efd1-122">Authorization</span></span> | <span data-ttu-id="5efd1-123">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="5efd1-123"></span></span> <span data-ttu-id="5efd1-124">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="5efd1-124">Required.</span></span> |
| <span data-ttu-id="5efd1-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5efd1-125">Content-Type</span></span> | <span data-ttu-id="5efd1-126">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="5efd1-126"></span></span> <span data-ttu-id="5efd1-127">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="5efd1-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5efd1-128">Основной текст запросов</span><span class="sxs-lookup"><span data-stu-id="5efd1-128">Request body</span></span>

<span data-ttu-id="5efd1-p105">Предоставьте в тексте запроса объект JSON с указанными ниже параметрами. **displayName** — это единственное доступное для записи свойство объекта [MailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="5efd1-p105">In the request body, provide a JSON object with the following parameters. **displayName** is the only writable property for a [MailFolder](../resources/mailfolder.md) object.</span></span>

| <span data-ttu-id="5efd1-131">Параметр</span><span class="sxs-lookup"><span data-stu-id="5efd1-131">Parameter</span></span> | <span data-ttu-id="5efd1-132">Тип</span><span class="sxs-lookup"><span data-stu-id="5efd1-132">Type</span></span> | <span data-ttu-id="5efd1-133">Описание</span><span class="sxs-lookup"><span data-stu-id="5efd1-133">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="5efd1-134">displayName</span><span class="sxs-lookup"><span data-stu-id="5efd1-134">displayName</span></span>|<span data-ttu-id="5efd1-135">String</span><span class="sxs-lookup"><span data-stu-id="5efd1-135">String</span></span>|<span data-ttu-id="5efd1-136">Отображаемое имя новой папки.</span><span class="sxs-lookup"><span data-stu-id="5efd1-136">The display name of the new folder.</span></span>|

## <a name="response"></a><span data-ttu-id="5efd1-137">Ответ</span><span class="sxs-lookup"><span data-stu-id="5efd1-137">Response</span></span>

<span data-ttu-id="5efd1-138">В случае успешного выполнения этот метод `201 Created` возвращает код отклика и объект [mailFolder](../resources/mailfolder.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="5efd1-138">If successful, this method returns `201 Created` response code and a [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5efd1-139">Пример</span><span class="sxs-lookup"><span data-stu-id="5efd1-139">Example</span></span>

#### <a name="request"></a><span data-ttu-id="5efd1-140">Запрос</span><span class="sxs-lookup"><span data-stu-id="5efd1-140">Request</span></span>

<span data-ttu-id="5efd1-141">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="5efd1-141">The following is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="5efd1-142">HTTP</span><span class="sxs-lookup"><span data-stu-id="5efd1-142">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_mailfolder_from_mailfolder"
}-->

```http
POST https://graph.microsoft.com/beta/me/mailFolders/{id}/childFolders
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value",
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="5efd1-143">C#</span><span class="sxs-lookup"><span data-stu-id="5efd1-143">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-mailfolder-from-mailfolder-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="5efd1-144">JavaScript</span><span class="sxs-lookup"><span data-stu-id="5efd1-144">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-mailfolder-from-mailfolder-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="5efd1-145">Цель — C</span><span class="sxs-lookup"><span data-stu-id="5efd1-145">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-mailfolder-from-mailfolder-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="5efd1-146">Java</span><span class="sxs-lookup"><span data-stu-id="5efd1-146">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/create-mailfolder-from-mailfolder-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a><span data-ttu-id="5efd1-147">Отклик</span><span class="sxs-lookup"><span data-stu-id="5efd1-147">Response</span></span>

<span data-ttu-id="5efd1-148">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="5efd1-148">The following is an example of the response.</span></span>

> <span data-ttu-id="5efd1-149">**Примечание.**  Объект ответа, показанный здесь, может быть сокращен для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="5efd1-149">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="5efd1-150">При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="5efd1-150">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 179

{
  "displayName": "displayName-value",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 99,
  "unreadItemCount": 99,
  "totalItemCount": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create mailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
