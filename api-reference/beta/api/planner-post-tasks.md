---
title: Создание объекта plannerTask
description: Используйте этот API, чтобы создать объект **plannerTask**.
localization_priority: Priority
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: f74e41e3c855fd6cf54019e2cfd13e36fce45b7e
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32538947"
---
# <a name="create-plannertask"></a><span data-ttu-id="dc457-103">Создание объекта plannerTask</span><span class="sxs-lookup"><span data-stu-id="dc457-103">Create plannerTask</span></span>

<span data-ttu-id="dc457-104">Используйте этот API, чтобы создать объект **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="dc457-104">Use this API to create a new **plannerTask**.</span></span>
## <a name="permissions"></a><span data-ttu-id="dc457-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="dc457-105">Permissions</span></span>
<span data-ttu-id="dc457-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc457-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dc457-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="dc457-108">Permission type</span></span>      | <span data-ttu-id="dc457-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="dc457-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dc457-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="dc457-110">Delegated (work or school account)</span></span> | <span data-ttu-id="dc457-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dc457-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="dc457-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="dc457-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dc457-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc457-113">Not supported.</span></span>    |
|<span data-ttu-id="dc457-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="dc457-114">Application</span></span> | <span data-ttu-id="dc457-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc457-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dc457-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="dc457-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /planner/tasks

```
## <a name="request-headers"></a><span data-ttu-id="dc457-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="dc457-117">Request headers</span></span>
| <span data-ttu-id="dc457-118">Имя</span><span class="sxs-lookup"><span data-stu-id="dc457-118">Name</span></span>       | <span data-ttu-id="dc457-119">Описание</span><span class="sxs-lookup"><span data-stu-id="dc457-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="dc457-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="dc457-120">Authorization</span></span>  | <span data-ttu-id="dc457-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="dc457-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dc457-123">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="dc457-123">Request body</span></span>
<span data-ttu-id="dc457-p103">Включите в текст запроса описание объекта [plannerTask](../resources/plannertask.md) в формате JSON. В качестве свойства **задачи Планировщика** planId необходимо указать идентификатор существующего объекта [plannerPlan](../resources/plannerplan.md).</span><span class="sxs-lookup"><span data-stu-id="dc457-p103">In the request body, supply a JSON representation of [plannerTask](../resources/plannertask.md) object. The **plannerTask** planId property must be set to an existing [plannerPlan](../resources/plannerplan.md) object's id.</span></span>

## <a name="response"></a><span data-ttu-id="dc457-126">Отклик</span><span class="sxs-lookup"><span data-stu-id="dc457-126">Response</span></span>

<span data-ttu-id="dc457-127">В случае успеха этот метод возвращает код ответа `201 Created` и объект [plannerTask](../resources/plannertask.md) в тексте ответа.</span><span class="sxs-lookup"><span data-stu-id="dc457-127">If successful, this method returns `201 Created` response code and [plannerTask](../resources/plannertask.md) object in the response body.</span></span>

<span data-ttu-id="dc457-p104">Этот метод может возвращать любые [коды состояния HTTP](/graph/errors). Приложения должны обрабатывать ошибки 400, 403 и 404, которые возникают чаще всего. Дополнительные сведения об этих ошибках см. в разделе [Основные ошибки Планировщика](../resources/planner-overview.md#common-planner-error-conditions).</span><span class="sxs-lookup"><span data-stu-id="dc457-p104">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="dc457-131">Пример</span><span class="sxs-lookup"><span data-stu-id="dc457-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dc457-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="dc457-132">Request</span></span>
<span data-ttu-id="dc457-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="dc457-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_plannertask_from_planner"
}-->
```http
POST https://graph.microsoft.com/v1.0/planner/tasks
Content-type: application/json
Content-length: 285

{
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "bucketId": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR",
  "title": "Update client list",
  "assignments": {
    "fbab97d0-4932-4511-b675-204639209557": {
      "@odata.type": "#microsoft.graph.plannerAssignment",
      "orderHint": " !"
    }
  },
}
```
<span data-ttu-id="dc457-134">Включите в текст запроса описание объекта [plannerTask](../resources/plannertask.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="dc457-134">In the request body, supply a JSON representation of [plannerTask](../resources/plannertask.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="dc457-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="dc457-135">Response</span></span>
<span data-ttu-id="dc457-p105">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="dc457-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerTask"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 677

{
  "createdBy": {
    "user": {
      "id": "6463a5ce-2119-4198-9f2a-628761df4a62"
    }
  },
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "bucketId": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR",
  "title": "Update client list",
  "orderHint": "85752723360752+",
  "createdDateTime": "2015-03-25T18:36:49.2407981Z",
  "assignments": {
    "fbab97d0-4932-4511-b675-204639209557": {
      "@odata.type": "#microsoft.graph.plannerAssignment",
      "assignedBy": {
        "user": {
          "id": "6463a5ce-2119-4198-9f2a-628761df4a62"
        }
      },
      "assignedDateTime": "2015-03-25T18:36:49.2407981Z",
      "orderHint": "RWk1"
    }
  },
  "id":"01gzSlKkIUSUl6DF_EilrmQAKDhh"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create plannerTask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
