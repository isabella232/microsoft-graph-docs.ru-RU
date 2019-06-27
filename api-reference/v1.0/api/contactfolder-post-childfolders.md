---
title: Создание объекта ContactFolder
description: 'Создание дочернего объекта contactFolder указанной папки. '
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 50c29561eb0ad55edb70cf003a6e8d2c4c5dc959
ms.sourcegitcommit: 0e1101d499f35b08aa2309e273871438b1774979
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2019
ms.locfileid: "35273915"
---
# <a name="create-contactfolder"></a><span data-ttu-id="9577e-103">Создание объекта ContactFolder</span><span class="sxs-lookup"><span data-stu-id="9577e-103">Create ContactFolder</span></span>

<span data-ttu-id="9577e-104">Создание дочернего объекта contactFolder указанной папки.</span><span class="sxs-lookup"><span data-stu-id="9577e-104">Create a new contactFolder as a child of a specified folder.</span></span> 

<span data-ttu-id="9577e-105">Вы также можете [создать объект contactFolder в папке контактов пользователя по умолчанию](user-post-contactfolders.md).</span><span class="sxs-lookup"><span data-stu-id="9577e-105">You can also [create a new contactFolder under the user's default contact folder](user-post-contactfolders.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="9577e-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="9577e-106">Permissions</span></span>
<span data-ttu-id="9577e-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9577e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9577e-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="9577e-109">Permission type</span></span>      | <span data-ttu-id="9577e-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="9577e-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9577e-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="9577e-111">Delegated (work or school account)</span></span> | <span data-ttu-id="9577e-112">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9577e-112">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="9577e-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="9577e-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9577e-114">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9577e-114">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="9577e-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="9577e-115">Application</span></span> | <span data-ttu-id="9577e-116">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9577e-116">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="9577e-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="9577e-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contactFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/contactFolders/{id}/childFolders
```
## <a name="request-headers"></a><span data-ttu-id="9577e-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="9577e-118">Request headers</span></span>
| <span data-ttu-id="9577e-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9577e-119">Header</span></span>       | <span data-ttu-id="9577e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9577e-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9577e-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="9577e-121">Authorization</span></span>  | <span data-ttu-id="9577e-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="9577e-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="9577e-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9577e-124">Content-Type</span></span>  | <span data-ttu-id="9577e-p103">application/json. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="9577e-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9577e-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="9577e-127">Request body</span></span>
<span data-ttu-id="9577e-128">Предоставьте в тексте запроса описание объекта [ContactFolder](../resources/contactfolder.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="9577e-128">In the request body, supply a JSON representation of [ContactFolder](../resources/contactfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="9577e-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="9577e-129">Response</span></span>

<span data-ttu-id="9577e-130">В случае успеха этот метод возвращает код отклика `201 Created` и объект [ContactFolder](../resources/contactfolder.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="9577e-130">If successful, this method returns `201 Created` response code and [ContactFolder](../resources/contactfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9577e-131">Пример</span><span class="sxs-lookup"><span data-stu-id="9577e-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9577e-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="9577e-132">Request</span></span>
<span data-ttu-id="9577e-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="9577e-133">Here is an example of the request.</span></span>
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
<span data-ttu-id="9577e-134">Предоставьте в тексте запроса описание объекта [contactFolder](../resources/contactfolder.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="9577e-134">In the request body, supply a JSON representation of [contactFolder](../resources/contactfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="9577e-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="9577e-135">Response</span></span>
<span data-ttu-id="9577e-p104">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="9577e-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
#### <a name="sdk-sample-code"></a><span data-ttu-id="9577e-139">Пример кода SDK</span><span class="sxs-lookup"><span data-stu-id="9577e-139">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="9577e-140">C#</span><span class="sxs-lookup"><span data-stu-id="9577e-140">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/create_contactfolder_from_contactfolder-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="9577e-141">Javascript</span><span class="sxs-lookup"><span data-stu-id="9577e-141">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/create_contactfolder_from_contactfolder-Javascript-snippets.md)]

# <a name="objective-ctabobjective-c"></a>[<span data-ttu-id="9577e-142">Цель — C</span><span class="sxs-lookup"><span data-stu-id="9577e-142">Objective-C</span></span>](#tab/objective-c)
[!INCLUDE [sample-code](../includes/create_contactfolder_from_contactfolder-Objective-C-snippets.md)]
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
    "Error: /api-reference/v1.0/api/contactfolder-post-childfolders.md:\r\n      BookmarkMissing: '[#tab/objective-c](Objective-C)'. Did you mean: #objective-c (score: 4)",
    "Error: /api-reference/v1.0/api/contactfolder-post-childfolders.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/v1.0/api/contactfolder-post-childfolders.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}-->
