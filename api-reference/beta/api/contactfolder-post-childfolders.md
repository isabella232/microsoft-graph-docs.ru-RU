---
title: Создание объекта ContactFolder
description: 'Создание дочернего объекта contactFolder указанной папки. '
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: e9b408591ba3e8b72f6a26ba289e3406e5f2df7e
ms.sourcegitcommit: b8d01acfc1cb7610a0e1f5c18065da415bae0777
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2019
ms.locfileid: "33591336"
---
# <a name="create-contactfolder"></a><span data-ttu-id="29f2c-103">Создание объекта ContactFolder</span><span class="sxs-lookup"><span data-stu-id="29f2c-103">Create ContactFolder</span></span>

<span data-ttu-id="29f2c-104">Создание дочернего объекта contactFolder указанной папки.</span><span class="sxs-lookup"><span data-stu-id="29f2c-104">Create a new contactFolder as a child of a specified folder.</span></span> 

<span data-ttu-id="29f2c-105">Вы также можете [создать объект contactFolder в папке контактов пользователя по умолчанию](user-post-contactfolders.md).</span><span class="sxs-lookup"><span data-stu-id="29f2c-105">You can also [create a new contactFolder under the user's default contact folder](user-post-contactfolders.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="29f2c-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="29f2c-106">Permissions</span></span>
<span data-ttu-id="29f2c-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="29f2c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="29f2c-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="29f2c-109">Permission type</span></span>      | <span data-ttu-id="29f2c-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="29f2c-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="29f2c-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="29f2c-111">Delegated (work or school account)</span></span> | <span data-ttu-id="29f2c-112">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="29f2c-112">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="29f2c-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="29f2c-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="29f2c-114">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="29f2c-114">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="29f2c-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="29f2c-115">Application</span></span> | <span data-ttu-id="29f2c-116">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="29f2c-116">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="29f2c-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="29f2c-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contactFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/contactFolders/{id}/childFolders
```
## <a name="request-headers"></a><span data-ttu-id="29f2c-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="29f2c-118">Request headers</span></span>
| <span data-ttu-id="29f2c-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="29f2c-119">Header</span></span>       | <span data-ttu-id="29f2c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="29f2c-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="29f2c-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="29f2c-121">Authorization</span></span>  | <span data-ttu-id="29f2c-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="29f2c-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="29f2c-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="29f2c-124">Content-Type</span></span>  | <span data-ttu-id="29f2c-p103">application/json. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="29f2c-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="29f2c-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="29f2c-127">Request body</span></span>
<span data-ttu-id="29f2c-128">Предоставьте в тексте запроса описание объекта [ContactFolder](../resources/contactfolder.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="29f2c-128">In the request body, supply a JSON representation of [ContactFolder](../resources/contactfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="29f2c-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="29f2c-129">Response</span></span>

<span data-ttu-id="29f2c-130">В случае успеха этот метод возвращает код отклика `201 Created` и объект [ContactFolder](../resources/contactfolder.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="29f2c-130">If successful, this method returns `201 Created` response code and [ContactFolder](../resources/contactfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="29f2c-131">Пример</span><span class="sxs-lookup"><span data-stu-id="29f2c-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="29f2c-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="29f2c-132">Request</span></span>
<span data-ttu-id="29f2c-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="29f2c-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contactfolder_from_contactfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/contactFolders/{id}/childFolders
Content-type: application/json
Content-length: 84

{
  "displayName": "displayName-value"
}
```
<span data-ttu-id="29f2c-134">Предоставьте в тексте запроса описание объекта [contactFolder](../resources/contactfolder.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="29f2c-134">In the request body, supply a JSON representation of [contactFolder](../resources/contactfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="29f2c-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="29f2c-135">Response</span></span>
<span data-ttu-id="29f2c-p104">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="29f2c-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 104

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value",
  "id": "id-value"
}
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="29f2c-139">Пример кода для SDK</span><span class="sxs-lookup"><span data-stu-id="29f2c-139">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="29f2c-140">Языках</span><span class="sxs-lookup"><span data-stu-id="29f2c-140">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/create_contactfolder_from_contactfolder-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="29f2c-141">Язык</span><span class="sxs-lookup"><span data-stu-id="29f2c-141">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/create_contactfolder_from_contactfolder-Javascript-snippets.md)]

---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create ContactFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/v1.0/api/contactfolder-post-childfolders.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/v1.0/api/contactfolder-post-childfolders.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}-->
