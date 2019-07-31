---
author: JeremyKelley
description: Создание ресурса listItem в списке.
ms.date: 09/11/2017
title: Создание записи в списке SharePoint
localization_priority: Normal
ms.prod: sharepoint
doc_type: apiPageType
ms.openlocfilehash: ebf41cf176956f90a40f75ac593714fcd6359e0b
ms.sourcegitcommit: 2c62457e57467b8d50f21b255b553106a9a5d8d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2019
ms.locfileid: "35993111"
---
# <a name="create-a-new-item-in-a-list"></a><span data-ttu-id="5ea4b-103">Создание элемента в списке</span><span class="sxs-lookup"><span data-stu-id="5ea4b-103">Create a new item in a list</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="5ea4b-104">Создание элемента [listItem][] в [списке][].</span><span class="sxs-lookup"><span data-stu-id="5ea4b-104">Create a new [listItem][] in a [list][].</span></span>

## <a name="permissions"></a><span data-ttu-id="5ea4b-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="5ea4b-105">Permissions</span></span>

<span data-ttu-id="5ea4b-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5ea4b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5ea4b-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="5ea4b-108">Permission type</span></span>      | <span data-ttu-id="5ea4b-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="5ea4b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5ea4b-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="5ea4b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="5ea4b-111">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5ea4b-111">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="5ea4b-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="5ea4b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5ea4b-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5ea4b-113">Not supported.</span></span>    |
|<span data-ttu-id="5ea4b-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="5ea4b-114">Application</span></span> | <span data-ttu-id="5ea4b-115">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5ea4b-115">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5ea4b-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="5ea4b-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items
```

## <a name="request-body"></a><span data-ttu-id="5ea4b-117">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="5ea4b-117">Request body</span></span>

<span data-ttu-id="5ea4b-118">В теле запроса укажите представление ресурса [listItem][], который необходимо создать, в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="5ea4b-118">In the request body, supply a JSON representation of the [listItem][] resource to create.</span></span>

## <a name="example"></a><span data-ttu-id="5ea4b-119">Пример</span><span class="sxs-lookup"><span data-stu-id="5ea4b-119">Example</span></span>

<span data-ttu-id="5ea4b-120">В примере ниже показано, как создать элемент списка общего назначения.</span><span class="sxs-lookup"><span data-stu-id="5ea4b-120">Here is an example of how to create a new generic list item.</span></span>


# <a name="httptabhttp"></a>[<span data-ttu-id="5ea4b-121">HTTP</span><span class="sxs-lookup"><span data-stu-id="5ea4b-121">HTTP</span></span>](#tab/http)
<!-- { "blockType": "request", "name": "create-listitem", "scopes": "sites.readwrite.all" } -->

```json
POST https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items
Content-Type: application/json

{
  "fields": {
    "Title": "Widget",
    "Color": "Purple",
    "Weight": 32
  }
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="5ea4b-122">C#</span><span class="sxs-lookup"><span data-stu-id="5ea4b-122">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-listitem-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="5ea4b-123">JavaScript</span><span class="sxs-lookup"><span data-stu-id="5ea4b-123">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-listitem-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="5ea4b-124">Цель — C</span><span class="sxs-lookup"><span data-stu-id="5ea4b-124">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-listitem-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="5ea4b-125">Java</span><span class="sxs-lookup"><span data-stu-id="5ea4b-125">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/create-listitem-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


## <a name="response"></a><span data-ttu-id="5ea4b-126">Ответ</span><span class="sxs-lookup"><span data-stu-id="5ea4b-126">Response</span></span>

<span data-ttu-id="5ea4b-127">При успешном выполнении этот метод возвращает объект [listItem][] для созданного элемента списка в теле ответа.</span><span class="sxs-lookup"><span data-stu-id="5ea4b-127">If successful, this method returns a [listItem][] in the response body for the created list item.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.listItem", "truncated": true } -->

```json
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "20",
  "createdDateTime": "2016-08-30T08:26:00Z",
  "createdBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "8606e4d5-d582-4f5f-aeba-7d7c18b20cfd"
    }
  },
  "lastModifiedDateTime": "2016-08-30T08:26:00Z",
  "lastModifiedBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "8606e4d5-d582-4f5f-aeba-7d7c18b20cfd"
    }
  }
}
```

<span data-ttu-id="5ea4b-128">**Примечание.** Ответ усечен для наглядности.</span><span class="sxs-lookup"><span data-stu-id="5ea4b-128">**Note:** The response object is truncated for clarity.</span></span> <span data-ttu-id="5ea4b-129">При фактическом вызове будут возвращены свойства, используемые по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5ea4b-129">Default properties will be returned from the actual call.</span></span>

[списке]: ../resources/list.md
[list]: ../resources/list.md
[listItem]: ../resources/listitem.md

<!--
{
  "type": "#page.annotation",
  "description": "Add a new item to a SharePoint list.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "ListItem/Create",
  "suppressions": [
  ]
}
-->
