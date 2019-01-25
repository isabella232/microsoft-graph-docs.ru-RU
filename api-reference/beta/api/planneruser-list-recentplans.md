---
title: Список recentPlans
description: Получение списка plannerPlans недавно просмотре пользователем. Недавно просматриваемые планы можно обновить, изменив plannerUser ресурсов.
author: TarkanSevilmis
localization_priority: Normal
ms.prod: planner
ms.openlocfilehash: b4a8e25a31ceb17f85aef139378fa3e3e9058ab4
ms.sourcegitcommit: 3d24047b3af46136734de2486b041e67a34f3d83
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "29528741"
---
# <a name="list-recentplans"></a><span data-ttu-id="43e1e-104">Список recentPlans</span><span class="sxs-lookup"><span data-stu-id="43e1e-104">List recentPlans</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="43e1e-105">Получение списка [plannerPlans](../resources/plannerplan.md) недавно просмотре пользователем.</span><span class="sxs-lookup"><span data-stu-id="43e1e-105">Retrieve a list of [plannerPlans](../resources/plannerplan.md) recently viewed by a user.</span></span> <span data-ttu-id="43e1e-106">Недавно просматриваемые планы можно обновить, [изменив plannerUser ресурсов](planneruser-update.md).</span><span class="sxs-lookup"><span data-stu-id="43e1e-106">You can update recently viewed plans by [updating the plannerUser resource](planneruser-update.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="43e1e-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="43e1e-107">Permissions</span></span>
<span data-ttu-id="43e1e-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="43e1e-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="43e1e-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="43e1e-110">Permission type</span></span>      | <span data-ttu-id="43e1e-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="43e1e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="43e1e-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="43e1e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="43e1e-113">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="43e1e-113">Group.Read.All</span></span>    |
|<span data-ttu-id="43e1e-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="43e1e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="43e1e-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="43e1e-115">Not supported.</span></span>    |
|<span data-ttu-id="43e1e-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="43e1e-116">Application</span></span> | <span data-ttu-id="43e1e-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="43e1e-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="43e1e-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="43e1e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/planner/recentPlans
GET /users/<id>/planner/recentPlans
```

## <a name="request-headers"></a><span data-ttu-id="43e1e-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="43e1e-119">Request headers</span></span>
| <span data-ttu-id="43e1e-120">Имя</span><span class="sxs-lookup"><span data-stu-id="43e1e-120">Name</span></span>      |<span data-ttu-id="43e1e-121">Описание</span><span class="sxs-lookup"><span data-stu-id="43e1e-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="43e1e-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="43e1e-122">Authorization</span></span>  | <span data-ttu-id="43e1e-p104">В заголовке указывается "Bearer {код}". Обязательный.</span><span class="sxs-lookup"><span data-stu-id="43e1e-p104">Bearer {code}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="43e1e-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="43e1e-125">Request body</span></span>
<span data-ttu-id="43e1e-126">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="43e1e-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="43e1e-127">Ответ</span><span class="sxs-lookup"><span data-stu-id="43e1e-127">Response</span></span>
<span data-ttu-id="43e1e-128">Успешно завершена, этот метод возвращает `200 OK` код ответа и коллекцию объектов [plannerPlan](../resources/plannerplan.md) в теле ответа.</span><span class="sxs-lookup"><span data-stu-id="43e1e-128">If successful, this method returns a `200 OK` response code and a collection of [plannerPlan](../resources/plannerplan.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="43e1e-129">Пример</span><span class="sxs-lookup"><span data-stu-id="43e1e-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="43e1e-130">Запрос</span><span class="sxs-lookup"><span data-stu-id="43e1e-130">Request</span></span>
<span data-ttu-id="43e1e-131">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="43e1e-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_recentplans"
}-->
```http
GET https://graph.microsoft.com/beta/me/planner/recentPlans
```
##### <a name="response"></a><span data-ttu-id="43e1e-132">Ответ</span><span class="sxs-lookup"><span data-stu-id="43e1e-132">Response</span></span>
<span data-ttu-id="43e1e-133">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="43e1e-133">The following is an example of the response.</span></span> 

><span data-ttu-id="43e1e-p105">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="43e1e-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlan",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 979

{
  "value": [
    {
      "@odata.etag": "W/\"JzEtUGxhbiAgQEBAQEBAQEBAQEBAQEBDXCc=\"",
      "createdBy": {
        "user": {
          "id": "dd8a8379-1ac1-4eee-861d-ec15f6fa3611"
        },
        "application": {
          "id": "09abbdfd-ed23-44ee-a2d9-a627aa1c90f3"
        }
      },
      "createdDateTime": "2015-10-14T00:57:28.4698344Z",
      "owner": "eacd01dd-84cc-4c12-bd8a-9a33e5aeed11",
      "title": "Budget Planning (2016)",
      "id": "uZWtCtli30CGoWLIWSat1mQAC0ai"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "List recentPlans",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/planneruser-list-recentplans.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
