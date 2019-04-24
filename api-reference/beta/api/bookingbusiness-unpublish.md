---
title: 'Букингбусинесс: Отмена публикации'
description: Сделайте страницу планирования этого бизнеса недоступной для внешних клиентов.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 0b6c8122d37e5f6cdb1698b0d86295156e3481a0
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32461845"
---
# <a name="bookingbusiness-unpublish"></a><span data-ttu-id="1a277-103">Букингбусинесс: Отмена публикации</span><span class="sxs-lookup"><span data-stu-id="1a277-103">bookingBusiness: unpublish</span></span>

 [!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="1a277-104">Сделайте страницу планирования этого бизнеса недоступной для внешних клиентов.</span><span class="sxs-lookup"><span data-stu-id="1a277-104">Make the scheduling page of this business not available to external customers.</span></span>

<span data-ttu-id="1a277-105">Задайте для \*\*\*\* свойства publishs значение false, а свойству **публикурл** — значение null.</span><span class="sxs-lookup"><span data-stu-id="1a277-105">Set the **isPublished** property to false, and **publicUrl** property to null.</span></span>

## <a name="permissions"></a><span data-ttu-id="1a277-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="1a277-106">Permissions</span></span>
<span data-ttu-id="1a277-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1a277-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1a277-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="1a277-109">Permission type</span></span>      | <span data-ttu-id="1a277-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="1a277-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1a277-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="1a277-111">Delegated (work or school account)</span></span> |  <span data-ttu-id="1a277-112">Резервирования. Manage. ALL</span><span class="sxs-lookup"><span data-stu-id="1a277-112">Bookings.Manage.All</span></span>   |
|<span data-ttu-id="1a277-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="1a277-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1a277-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1a277-114">Not supported.</span></span>   |
|<span data-ttu-id="1a277-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="1a277-115">Application</span></span> | <span data-ttu-id="1a277-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1a277-116">Not supported.</span></span>  |

## <a name="http-request"></a><span data-ttu-id="1a277-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="1a277-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /bookingBusinesses/{id}/unpublish

```
## <a name="request-headers"></a><span data-ttu-id="1a277-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="1a277-118">Request headers</span></span>
| <span data-ttu-id="1a277-119">Имя</span><span class="sxs-lookup"><span data-stu-id="1a277-119">Name</span></span>       | <span data-ttu-id="1a277-120">Описание</span><span class="sxs-lookup"><span data-stu-id="1a277-120">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1a277-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="1a277-121">Authorization</span></span>  | <span data-ttu-id="1a277-122">Bearer {code}</span><span class="sxs-lookup"><span data-stu-id="1a277-122">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="1a277-123">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="1a277-123">Request body</span></span>

## <a name="response"></a><span data-ttu-id="1a277-124">Отклик</span><span class="sxs-lookup"><span data-stu-id="1a277-124">Response</span></span>
<span data-ttu-id="1a277-p102">В случае успешного выполнения этот метод возвращает код отклика `204 No content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="1a277-p102">If successful, this method returns `204 No content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1a277-127">Пример</span><span class="sxs-lookup"><span data-stu-id="1a277-127">Example</span></span>
<span data-ttu-id="1a277-128">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="1a277-128">The following is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="1a277-129">Запрос</span><span class="sxs-lookup"><span data-stu-id="1a277-129">Request</span></span>
<span data-ttu-id="1a277-130">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="1a277-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "bookingbusiness_unpublish"
}-->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/unpublish
```

##### <a name="response"></a><span data-ttu-id="1a277-131">Отклик</span><span class="sxs-lookup"><span data-stu-id="1a277-131">Response</span></span>
<span data-ttu-id="1a277-132">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="1a277-132">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "bookingBusiness: unpublish",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/bookingbusiness-unpublish.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
