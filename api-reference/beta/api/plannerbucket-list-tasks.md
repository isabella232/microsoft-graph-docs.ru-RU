---
title: Перечисление задач
description: Получение списка объектов **plannerTask**, связанных с объектом plannerBucket.
ms.openlocfilehash: 679da04497cf17e64e7764abcbed5b4c9992bf9f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27079511"
---
# <a name="list-tasks"></a><span data-ttu-id="e016a-103">Перечисление задач</span><span class="sxs-lookup"><span data-stu-id="e016a-103">List tasks</span></span>

> <span data-ttu-id="e016a-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="e016a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e016a-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e016a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e016a-106">Получение списка объектов **plannerTask**, связанных с объектом [plannerBucket](../resources/plannerbucket.md).</span><span class="sxs-lookup"><span data-stu-id="e016a-106">Retrieve a list of **plannerTask** objects associated to a [plannerBucket](../resources/plannerbucket.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="e016a-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="e016a-107">Permissions</span></span>
<span data-ttu-id="e016a-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e016a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e016a-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="e016a-110">Permission type</span></span>      | <span data-ttu-id="e016a-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="e016a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e016a-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="e016a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e016a-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e016a-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="e016a-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="e016a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e016a-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e016a-115">Not supported.</span></span>    |
|<span data-ttu-id="e016a-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="e016a-116">Application</span></span> | <span data-ttu-id="e016a-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e016a-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e016a-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="e016a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/buckets/<id>/tasks
```

## <a name="request-headers"></a><span data-ttu-id="e016a-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="e016a-119">Request headers</span></span>
| <span data-ttu-id="e016a-120">Имя</span><span class="sxs-lookup"><span data-stu-id="e016a-120">Name</span></span>      |<span data-ttu-id="e016a-121">Описание</span><span class="sxs-lookup"><span data-stu-id="e016a-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="e016a-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="e016a-122">Authorization</span></span>  | <span data-ttu-id="e016a-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e016a-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e016a-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="e016a-125">Request body</span></span>
<span data-ttu-id="e016a-126">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="e016a-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e016a-127">Ответ</span><span class="sxs-lookup"><span data-stu-id="e016a-127">Response</span></span>

<span data-ttu-id="e016a-128">В случае успеха этот метод возвращает код ответа `200 OK` и коллекцию объектов [plannerTask](../resources/plannertask.md) в тексте ответа.</span><span class="sxs-lookup"><span data-stu-id="e016a-128">If successful, this method returns a `200 OK` response code and collection of [plannerTask](../resources/plannertask.md) objects in the response body.</span></span>

<span data-ttu-id="e016a-p104">Этот метод может возвращать любые [коды состояния HTTP](/graph/errors). Приложения должны обрабатывать ошибки 403 и 404, которые возникают чаще всего. Дополнительные сведения об этих ошибках см. в разделе [Основные ошибки Планировщика](../resources/planner-overview.md#common-planner-error-conditions).</span><span class="sxs-lookup"><span data-stu-id="e016a-p104">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="e016a-132">Пример</span><span class="sxs-lookup"><span data-stu-id="e016a-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e016a-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="e016a-133">Request</span></span>
<span data-ttu-id="e016a-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="e016a-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_tasks"
}-->
```http
GET https://graph.microsoft.com/beta/planner/buckets/gcrYAaAkgU2EQUvpkNNXLGQAGTtu/tasks
```
##### <a name="response"></a><span data-ttu-id="e016a-135">Ответ</span><span class="sxs-lookup"><span data-stu-id="e016a-135">Response</span></span>
<span data-ttu-id="e016a-p105">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
</span><span class="sxs-lookup"><span data-stu-id="e016a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerTask",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 833

{
  "value": [
    {
      "createdBy": {
        "user": {
          "id": "6463a5ce-2119-4198-9f2a-628761df4a62"
        }
      },
      "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
      "bucketId": "gcrYAaAkgU2EQUvpkNNXLGQAGTtu",
      "title": "title-value",
      "orderHint": "9223370609546166567W",
      "assigneePriority": "90057581\"",
      "createdDateTime": "2015-03-25T18:36:49.2407981Z",
      "assignments": {
        "fbab97d0-4932-4511-b675-204639209557": {
          "@odata.type": "#microsoft.graph.plannerassignment",
          "assignedBy": {
            "user": {
              "id": "1e9955d2-6acd-45bf-86d3-b546fdc795eb"
            }
          },
          "assignedDateTime": "2015-03-25T18:38:21.956Z",
          "orderHint": "RWk1"
         }
      },
      "id":"01gzSlKkIUSUl6DF_EilrmQAKDhh"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List tasks",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->