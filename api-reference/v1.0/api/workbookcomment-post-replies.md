---
title: Создание Воркбуккомментрепли
description: Используйте этот API для создания нового Воркбуккомментрепли.
localization_priority: Normal
author: grangeryy
ms.prod: ''
doc_type: apiPageType
ms.openlocfilehash: 0ec38cda1c2c138f4ae2168fbfe60f9d61b890fd
ms.sourcegitcommit: d8a58221ed1f2b7b7073fd621da4737e11ba53c5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/11/2019
ms.locfileid: "36839089"
---
# <a name="create-workbookcommentreply"></a><span data-ttu-id="7aec0-103">Создание Воркбуккомментрепли</span><span class="sxs-lookup"><span data-stu-id="7aec0-103">Create workbookCommentReply</span></span>

<span data-ttu-id="7aec0-104">Создание нового объекта [воркбуккомментрепли](../resources/workbookcommentreply.md) .</span><span class="sxs-lookup"><span data-stu-id="7aec0-104">Create a new [workbookCommentReply](../resources/workbookcommentreply.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="7aec0-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="7aec0-105">Permissions</span></span>

<span data-ttu-id="7aec0-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7aec0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7aec0-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="7aec0-108">Permission type</span></span>                        | <span data-ttu-id="7aec0-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="7aec0-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="7aec0-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7aec0-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="7aec0-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7aec0-111">Files.ReadWrite</span></span> |
| <span data-ttu-id="7aec0-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="7aec0-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7aec0-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7aec0-113">Not supported.</span></span> |
| <span data-ttu-id="7aec0-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="7aec0-114">Application</span></span>                            | <span data-ttu-id="7aec0-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7aec0-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7aec0-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="7aec0-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /workbook/comments/{id}/replies
```

## <a name="request-headers"></a><span data-ttu-id="7aec0-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="7aec0-117">Request headers</span></span>

| <span data-ttu-id="7aec0-118">Имя</span><span class="sxs-lookup"><span data-stu-id="7aec0-118">Name</span></span>          | <span data-ttu-id="7aec0-119">Описание</span><span class="sxs-lookup"><span data-stu-id="7aec0-119">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="7aec0-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="7aec0-120">Authorization</span></span> | <span data-ttu-id="7aec0-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7aec0-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7aec0-123">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="7aec0-123">Request body</span></span>

<span data-ttu-id="7aec0-124">В тексте запроса добавьте представление объекта [воркбуккомментрепли](../resources/workbookcommentreply.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="7aec0-124">In the request body, supply a JSON representation of a [workbookCommentReply](../resources/workbookcommentreply.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="7aec0-125">Отклик</span><span class="sxs-lookup"><span data-stu-id="7aec0-125">Response</span></span>

<span data-ttu-id="7aec0-126">В случае успешного выполнения этот метод возвращает `201 Created` код отклика и новый объект [воркбуккомментрепли](../resources/workbookcommentreply.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="7aec0-126">If successful, this method returns a `201 Created` response code and a new [workbookCommentReply](../resources/workbookcommentreply.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="7aec0-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="7aec0-127">Examples</span></span>

### <a name="request"></a><span data-ttu-id="7aec0-128">Запрос</span><span class="sxs-lookup"><span data-stu-id="7aec0-128">Request</span></span>

<span data-ttu-id="7aec0-129">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="7aec0-129">The following is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="7aec0-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="7aec0-130">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_workbookcommentreply_from_workbookcomment"
}-->

```http
POST https://graph.microsoft.com/v1.0/drive/root/workbook/comments/{id}/replies
Content-type: application/json

{
  "content": "This is my reply to the comment.",
  "contentType": "plain"
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="7aec0-131">C#</span><span class="sxs-lookup"><span data-stu-id="7aec0-131">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-workbookcommentreply-from-workbookcomment-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="7aec0-132">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7aec0-132">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-workbookcommentreply-from-workbookcomment-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="7aec0-133">Цель — C</span><span class="sxs-lookup"><span data-stu-id="7aec0-133">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-workbookcommentreply-from-workbookcomment-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="7aec0-134">Java</span><span class="sxs-lookup"><span data-stu-id="7aec0-134">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/create-workbookcommentreply-from-workbookcomment-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a><span data-ttu-id="7aec0-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="7aec0-135">Response</span></span>

<span data-ttu-id="7aec0-136">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="7aec0-136">The following is an example of the response.</span></span>

> <span data-ttu-id="7aec0-p103">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="7aec0-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookCommentReply"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "content": "This is my reply to the comment.",
  "contentType": "plain",
  "id": "{97A21473-8339-4BF0-BCB6-F55E4909FFB8}"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create workbookCommentReply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->