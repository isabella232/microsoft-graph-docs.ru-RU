---
title: Удаление объекта MailFolder
description: Удаление указанного mailFolder или Маилсеарчфолдер.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: 9d48b3c2fb19f9bb9696c4e7e93b8688e03b6f21
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "36342938"
---
# <a name="delete-mailfolder"></a><span data-ttu-id="67f10-103">Удаление объекта MailFolder</span><span class="sxs-lookup"><span data-stu-id="67f10-103">Delete mailFolder</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="67f10-104">Удаление указанного [mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="67f10-104">Delete the specified [mailFolder](../resources/mailfolder.md).</span></span> <span data-ttu-id="67f10-105">Папка может быть [маилсеарчфолдер](../resources/mailsearchfolder.md).</span><span class="sxs-lookup"><span data-stu-id="67f10-105">The folder can be a [mailSearchFolder](../resources/mailsearchfolder.md).</span></span>

<span data-ttu-id="67f10-106">Вы можете указать почтовую папку по ее ИДЕНТИФИКАТОРу папки или по известному [имени папки](../resources/mailfolder.md), если она существует.</span><span class="sxs-lookup"><span data-stu-id="67f10-106">You can specify a mail folder by its folder ID, or by its [well-known folder name](../resources/mailfolder.md), if one exists.</span></span> 

><span data-ttu-id="67f10-107">**Note (Примечание** ) Удаление элементов из папки "удаления элементов с возможностью восстановления" может быть недоступно (представлено известным именем `recoverableitemsdeletions`папки).</span><span class="sxs-lookup"><span data-stu-id="67f10-107">**Note** You may not be able to delete items in the recoverable items deletions folder (represented by the well-known folder name `recoverableitemsdeletions`).</span></span> <span data-ttu-id="67f10-108">Дополнительные сведения см. в статье [Хранение удаленных](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) элементов и [Очистка удаленных элементов](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) .</span><span class="sxs-lookup"><span data-stu-id="67f10-108">See [Deleted item retention](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) and [Clean up deleted items](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) for more information.</span></span>

## <a name="permissions"></a><span data-ttu-id="67f10-109">Разрешения</span><span class="sxs-lookup"><span data-stu-id="67f10-109">Permissions</span></span>
<span data-ttu-id="67f10-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="67f10-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="67f10-112">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="67f10-112">Permission type</span></span>      | <span data-ttu-id="67f10-113">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="67f10-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="67f10-114">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="67f10-114">Delegated (work or school account)</span></span> | <span data-ttu-id="67f10-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="67f10-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="67f10-116">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="67f10-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="67f10-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="67f10-117">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="67f10-118">Для приложений</span><span class="sxs-lookup"><span data-stu-id="67f10-118">Application</span></span> | <span data-ttu-id="67f10-119">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="67f10-119">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="67f10-120">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="67f10-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="67f10-121">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="67f10-121">Request headers</span></span>
| <span data-ttu-id="67f10-122">Имя</span><span class="sxs-lookup"><span data-stu-id="67f10-122">Name</span></span>       | <span data-ttu-id="67f10-123">Тип</span><span class="sxs-lookup"><span data-stu-id="67f10-123">Type</span></span> | <span data-ttu-id="67f10-124">Описание</span><span class="sxs-lookup"><span data-stu-id="67f10-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="67f10-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="67f10-125">Authorization</span></span>  | <span data-ttu-id="67f10-126">string</span><span class="sxs-lookup"><span data-stu-id="67f10-126">string</span></span>  | <span data-ttu-id="67f10-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="67f10-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="67f10-129">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="67f10-129">Request body</span></span>
<span data-ttu-id="67f10-130">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="67f10-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="67f10-131">Отклик</span><span class="sxs-lookup"><span data-stu-id="67f10-131">Response</span></span>
<span data-ttu-id="67f10-p105">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="67f10-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="67f10-134">Пример</span><span class="sxs-lookup"><span data-stu-id="67f10-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="67f10-135">Запрос</span><span class="sxs-lookup"><span data-stu-id="67f10-135">Request</span></span>
<span data-ttu-id="67f10-136">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="67f10-136">The following is an example of the request.</span></span>

# <a name="httptabhttp"></a>[<span data-ttu-id="67f10-137">HTTP</span><span class="sxs-lookup"><span data-stu-id="67f10-137">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_mailfolder"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/mailFolders/AAMkAGVmMDEzM/
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="67f10-138">C#</span><span class="sxs-lookup"><span data-stu-id="67f10-138">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-mailfolder-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="67f10-139">JavaScript</span><span class="sxs-lookup"><span data-stu-id="67f10-139">JavaScript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-mailfolder-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="67f10-140">Цель — C</span><span class="sxs-lookup"><span data-stu-id="67f10-140">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-mailfolder-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="67f10-141">Java</span><span class="sxs-lookup"><span data-stu-id="67f10-141">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-mailfolder-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a><span data-ttu-id="67f10-142">Отклик</span><span class="sxs-lookup"><span data-stu-id="67f10-142">Response</span></span>
<span data-ttu-id="67f10-143">Ниже приведен пример ответа.</span><span class="sxs-lookup"><span data-stu-id="67f10-143">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Delete mailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
