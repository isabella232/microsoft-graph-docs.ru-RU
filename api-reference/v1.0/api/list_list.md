---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: "Создание списка списков SharePoint на сайте"
ms.openlocfilehash: 8c3d8da3e8dc4ab3aa2f399eb09d916ea602e1c5
ms.sourcegitcommit: 339070a20730bc4d363da7eb346d5f3c1e1d6c3e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="enumerate-lists-in-a-site"></a><span data-ttu-id="9da68-102">Перечисление списков на сайте</span><span class="sxs-lookup"><span data-stu-id="9da68-102">Enumerate lists in a site</span></span>

<span data-ttu-id="9da68-103">Получение коллекции [списков][] для [сайта][].</span><span class="sxs-lookup"><span data-stu-id="9da68-103">Get the collection of [lists][] for a [site][].</span></span>

[lists]: ../resources/list.md
[site]: ../resources/site.md

## <a name="permissions"></a><span data-ttu-id="9da68-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="9da68-106">Permissions</span></span>

<span data-ttu-id="9da68-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9da68-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9da68-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="9da68-109">Permission type</span></span>      | <span data-ttu-id="9da68-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="9da68-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9da68-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="9da68-111">Delegated (work or school account)</span></span> | <span data-ttu-id="9da68-112">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9da68-112">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="9da68-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="9da68-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9da68-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9da68-114">Not supported.</span></span>    |
|<span data-ttu-id="9da68-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="9da68-115">Application</span></span> | <span data-ttu-id="9da68-116">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9da68-116">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9da68-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="9da68-117">HTTP request</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists
```

## <a name="example"></a><span data-ttu-id="9da68-118">Пример</span><span class="sxs-lookup"><span data-stu-id="9da68-118">Example</span></span>

#### <a name="request"></a><span data-ttu-id="9da68-119">Запрос</span><span class="sxs-lookup"><span data-stu-id="9da68-119">Request</span></span>

<!-- { "blockType": "request", "name": "enum-lists", "scopes": "sites.read.all service.sharepoint" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}/lists
```

##### <a name="response"></a><span data-ttu-id="9da68-120">Отклик</span><span class="sxs-lookup"><span data-stu-id="9da68-120">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.list", "isCollection": true, "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "b57af081-936c-4803-a120-d94887b03864",
      "name": "Documents",
      "createdDateTime": "2016-08-30T08:32:00Z",
      "lastModifiedDateTime": "2016-08-30T08:32:00Z",
      "list": {
        "hidden": false,
        "template": "documentLibrary"
       }
    },
    {
      "id": "1234-112-112-4",
      "name": "MicroFeed",
      "createdDateTime": "2016-08-30T08:32:00Z",
      "lastModifiedDateTime": "2016-08-30T08:32:00Z",
      "list": {
        "hidden": false,
        "template": "genericList"
       }
    }
  ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Lists/Enumerate"
} -->
