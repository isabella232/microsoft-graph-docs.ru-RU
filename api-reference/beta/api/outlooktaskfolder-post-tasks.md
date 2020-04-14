---
title: Создание объекта outlookTask
description: Создание задачи Outlook в указанной папке задач.
author: mashriv
localization_priority: Normal
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: ea84b119fcb92bf6d97510a93fbe25a30bb9de42
ms.sourcegitcommit: bbcf074f0be9d5e02f84c290122850cc5968fb1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2020
ms.locfileid: "43389641"
---
# <a name="create-outlooktask"></a><span data-ttu-id="765c7-103">Создание объекта outlookTask</span><span class="sxs-lookup"><span data-stu-id="765c7-103">Create outlookTask</span></span>

<span data-ttu-id="765c7-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="765c7-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="765c7-105">Создание задачи Outlook в указанной папке задач.</span><span class="sxs-lookup"><span data-stu-id="765c7-105">Create an Outlook task in the specified task folder.</span></span>

<span data-ttu-id="765c7-106">Метод POST всегда игнорирует часть времени **startDateTime** и **дуедатетиме** в теле запроса и предполагает, что время будет всегда в полночь в заданном часовом поясе.</span><span class="sxs-lookup"><span data-stu-id="765c7-106">The POST method always ignores the time portion of **startDateTime** and **dueDateTime** in the request body, and assumes the time to be always midnight in the specified time zone.</span></span>

## <a name="permissions"></a><span data-ttu-id="765c7-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="765c7-107">Permissions</span></span>
<span data-ttu-id="765c7-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="765c7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="765c7-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="765c7-110">Permission type</span></span>      | <span data-ttu-id="765c7-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="765c7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="765c7-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="765c7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="765c7-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="765c7-113">Not supported.</span></span>    |
|<span data-ttu-id="765c7-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="765c7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="765c7-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="765c7-115">Not supported.</span></span>    |
|<span data-ttu-id="765c7-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="765c7-116">Application</span></span> | <span data-ttu-id="765c7-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="765c7-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="765c7-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="765c7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/outlook/taskFolders/{id}/tasks
POST /me/outlook/taskGroups/{id}/taskFolders/{id}/tasks
POST /users/{id|userPrincipalName}/outlook/taskFolders/{id}/tasks
POST /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}/tasks
```
## <a name="request-headers"></a><span data-ttu-id="765c7-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="765c7-119">Request headers</span></span>
| <span data-ttu-id="765c7-120">Имя</span><span class="sxs-lookup"><span data-stu-id="765c7-120">Name</span></span>       | <span data-ttu-id="765c7-121">Описание</span><span class="sxs-lookup"><span data-stu-id="765c7-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="765c7-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="765c7-122">Authorization</span></span>  | <span data-ttu-id="765c7-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="765c7-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="765c7-125">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="765c7-125">Prefer: outlook.timezone</span></span> | <span data-ttu-id="765c7-126">Задает часовой пояс для свойств времени в отклике в формате UTC, если заголовок не указан.</span><span class="sxs-lookup"><span data-stu-id="765c7-126">Specifies the time zone for time properties in the response, which would be in UTC if this header is not specified.</span></span> <span data-ttu-id="765c7-127">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="765c7-127">Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="765c7-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="765c7-128">Request body</span></span>
<span data-ttu-id="765c7-129">В тексте запроса добавьте представление объекта [outlookTask](../resources/outlooktask.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="765c7-129">In the request body, supply a JSON representation of [outlookTask](../resources/outlooktask.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="765c7-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="765c7-130">Response</span></span>

<span data-ttu-id="765c7-131">В случае успешного выполнения этот метод `201 Created` возвращает код отклика и объект [outlookTask](../resources/outlooktask.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="765c7-131">If successful, this method returns `201 Created` response code and [outlookTask](../resources/outlooktask.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="765c7-132">Пример</span><span class="sxs-lookup"><span data-stu-id="765c7-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="765c7-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="765c7-133">Request</span></span>
<span data-ttu-id="765c7-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="765c7-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_outlooktask_from_outlooktaskfolder"
}-->
```http
POST https://graph.microsoft.com/beta/me/taskfolders('AAMkADIyAAAhrbPXAAA=')/tasks
Content-type: application/json
Content-length: 376

{
  "subject": "Shop for dinner",
  "startDateTime": {
      "dateTime": "2016-04-23T18:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "dueDateTime":  {
      "dateTime": "2016-04-25T13:00:00",
      "timeZone": "Pacific Standard Time"
  }
}
```
<span data-ttu-id="765c7-135">В тексте запроса добавьте представление объекта [outlookTask](../resources/outlooktask.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="765c7-135">In the request body, supply a JSON representation of [outlookTask](../resources/outlooktask.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="765c7-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="765c7-136">Response</span></span>
<span data-ttu-id="765c7-137">Метод POST игнорирует часть времени в теле запроса и принимает время в полночь всегда в заданном часовом поясе (PST).</span><span class="sxs-lookup"><span data-stu-id="765c7-137">The POST method ignores the time portion in the request body and assumes the time to be always midnight in the specified time zone (PST).</span></span> <span data-ttu-id="765c7-138">Затем по умолчанию метод POST преобразует и отображает все свойства, связанные с датой, в формате UTC в ответе.</span><span class="sxs-lookup"><span data-stu-id="765c7-138">Then, by default, the POST method converts and shows all the date-related properties in UTC in the response.</span></span>

<span data-ttu-id="765c7-p105">Примечание. Представленный здесь объект отклика может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="765c7-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTask"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 376

{
  "createdDateTime": "2016-04-22T05:44:01.2012012Z",
  "lastModifiedDateTime": "2016-04-22T05:44:02.9980882Z",
  "changeKey": "1/KC9Vmu40G3DwB6Lgs7MAAAIOJMxw==",
  "categories": [ ],
  "assignedTo": "null",
  "body": {
    "contentType": "Text",
    "content": ""
  },
  "completedDateTime": null,
  "dueDateTime": {
    "dateTime": "2016-04-25T07:00:00.0000000",
    "timeZone": "UTC"
  },
  "hasAttachments":false,
  "importance": "Normal",
  "isReminderOn": false,
  "owner": "Administrator",
  "parentFolderId": "AQMkADA1MTkAAAAIBEgAAAA==",
  "recurrence": null,
  "reminderDateTime": null,
  "sensitivity": "Normal",
  "startDateTime": {
    "dateTime": "2016-04-23T07:00:00.0000000",
    "timeZone": "UTC"
  },
  "status": "NotStarted",
  "subject": "Shop for dinner"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create outlookTask",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
