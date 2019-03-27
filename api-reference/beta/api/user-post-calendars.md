---
title: Создание объекта Calendar
description: С помощью этого API можно создать календарь для экземпляра user.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: afbb37d9394f2c08c94c6c8f41c56431e6938831
ms.sourcegitcommit: a17ad12b05fbad86fc21ea4384c36e3b14e543c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2019
ms.locfileid: "30869332"
---
# <a name="create-calendar"></a><span data-ttu-id="cc8ea-103">Создание объекта Calendar</span><span class="sxs-lookup"><span data-stu-id="cc8ea-103">Create Calendar</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="cc8ea-104">С помощью этого API можно создать календарь для экземпляра [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="cc8ea-104">Use this API to create a new calendar for a [user](../resources/user.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="cc8ea-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="cc8ea-105">Permissions</span></span>
<span data-ttu-id="cc8ea-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cc8ea-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cc8ea-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="cc8ea-108">Permission type</span></span>      | <span data-ttu-id="cc8ea-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="cc8ea-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cc8ea-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="cc8ea-110">Delegated (work or school account)</span></span> | <span data-ttu-id="cc8ea-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cc8ea-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="cc8ea-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="cc8ea-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cc8ea-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cc8ea-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="cc8ea-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="cc8ea-114">Application</span></span> | <span data-ttu-id="cc8ea-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cc8ea-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="cc8ea-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="cc8ea-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/calendars
POST /users/{id | userPrincipalName}/calendars
```
## <a name="request-headers"></a><span data-ttu-id="cc8ea-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="cc8ea-117">Request headers</span></span>
| <span data-ttu-id="cc8ea-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cc8ea-118">Header</span></span>       | <span data-ttu-id="cc8ea-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cc8ea-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="cc8ea-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="cc8ea-120">Authorization</span></span>  | <span data-ttu-id="cc8ea-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="cc8ea-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="cc8ea-123">Content-Type</span></span>  | <span data-ttu-id="cc8ea-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cc8ea-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="cc8ea-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="cc8ea-125">Request body</span></span>
<span data-ttu-id="cc8ea-126">Предоставьте в тексте запроса описание объекта [calendar](../resources/calendar.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-126">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="cc8ea-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="cc8ea-127">Response</span></span>

<span data-ttu-id="cc8ea-128">В случае успеха этот метод возвращает код отклика `201 Created` и объект [calendar](../resources/calendar.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-128">If successful, this method returns `201 Created` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cc8ea-129">Пример</span><span class="sxs-lookup"><span data-stu-id="cc8ea-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cc8ea-130">Запрос</span><span class="sxs-lookup"><span data-stu-id="cc8ea-130">Request</span></span>
<span data-ttu-id="cc8ea-131">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_calendar_from_user"
}-->
```http
POST https://graph.microsoft.com/beta/me/calendars
Content-type: application/json

{
  "name": "Volunteer"
}

```
<span data-ttu-id="cc8ea-132">Предоставьте в тексте запроса описание объекта [calendar](../resources/calendar.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-132">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="cc8ea-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="cc8ea-133">Response</span></span>
<span data-ttu-id="cc8ea-p103">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#me/calendars/$entity",
    "@odata.id":"https://graph.microsoft.com/beta/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/calendars('AAMkADJmMVAAA=')",
    "id":"AAMkADJmMVAAA=",
    "name":"Volunteer",
    "color":"auto",
    "isDefaultCalendar":false,
    "changeKey":"DxYSthXJXEWwAQSYQnXvIgAAIxGttg==",
    "canShare":true,
    "canViewPrivateItems":true,
    "hexColor": "",
    "isShared":false,
    "isSharedWithMe":false,
    "canEdit":true,
    "owner":{
        "name":"Samantha Booth",
        "address":"samanthab@adatum.onmicrosoft.com"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create Calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/user-post-calendars.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
