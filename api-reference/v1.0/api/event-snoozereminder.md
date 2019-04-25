---
title: 'event: snoozeReminder'
description: ОтЛожить напоминание о событии в календаре пользователя до нового времени.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: d3f8ffab576182f5e67dad49e34c67d886fe0bde
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32584308"
---
# <a name="event-snoozereminder"></a><span data-ttu-id="8915b-103">event: snoozeReminder</span><span class="sxs-lookup"><span data-stu-id="8915b-103">event: snoozeReminder</span></span>

<span data-ttu-id="8915b-104">ОтЛожить напоминание о [событии](../resources/event.md) в календаре [](../resources/calendar.md) пользователя до нового времени.</span><span class="sxs-lookup"><span data-stu-id="8915b-104">Postpone a reminder for an [event](../resources/event.md) in a user [calendar](../resources/calendar.md) until a new time.</span></span>

## <a name="permissions"></a><span data-ttu-id="8915b-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="8915b-105">Permissions</span></span>
<span data-ttu-id="8915b-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8915b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8915b-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="8915b-108">Permission type</span></span>      | <span data-ttu-id="8915b-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="8915b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8915b-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8915b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="8915b-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8915b-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="8915b-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="8915b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8915b-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8915b-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="8915b-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="8915b-114">Application</span></span> | <span data-ttu-id="8915b-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8915b-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="8915b-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="8915b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/events/{id}/snoozeReminder

POST /me/calendar/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendar/events/{id}/snoozeReminder

POST /me/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/snoozeReminder

POST /me/calendargroup/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/snoozeReminder

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/snoozeReminder
```
## <a name="request-headers"></a><span data-ttu-id="8915b-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="8915b-117">Request headers</span></span>
| <span data-ttu-id="8915b-118">Имя</span><span class="sxs-lookup"><span data-stu-id="8915b-118">Name</span></span>       | <span data-ttu-id="8915b-119">Тип</span><span class="sxs-lookup"><span data-stu-id="8915b-119">Type</span></span> | <span data-ttu-id="8915b-120">Описание</span><span class="sxs-lookup"><span data-stu-id="8915b-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="8915b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="8915b-121">Authorization</span></span>  | <span data-ttu-id="8915b-122">string</span><span class="sxs-lookup"><span data-stu-id="8915b-122">string</span></span>  | <span data-ttu-id="8915b-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="8915b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8915b-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8915b-125">Content-Type</span></span> | <span data-ttu-id="8915b-126">string</span><span class="sxs-lookup"><span data-stu-id="8915b-126">string</span></span>  | <span data-ttu-id="8915b-p103">Характер данных в теле объекта. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="8915b-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8915b-129">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="8915b-129">Request body</span></span>
<span data-ttu-id="8915b-130">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="8915b-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="8915b-131">Параметр</span><span class="sxs-lookup"><span data-stu-id="8915b-131">Parameter</span></span>    | <span data-ttu-id="8915b-132">Тип</span><span class="sxs-lookup"><span data-stu-id="8915b-132">Type</span></span>   |<span data-ttu-id="8915b-133">Описание</span><span class="sxs-lookup"><span data-stu-id="8915b-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8915b-134">newReminderTime</span><span class="sxs-lookup"><span data-stu-id="8915b-134">newReminderTime</span></span>|<span data-ttu-id="8915b-135">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="8915b-135">DateTimeTimeZone</span></span>|<span data-ttu-id="8915b-136">Новые дата и время для активации напоминания.</span><span class="sxs-lookup"><span data-stu-id="8915b-136">The new date and time to trigger the reminder.</span></span>|

## <a name="response"></a><span data-ttu-id="8915b-137">Отклик</span><span class="sxs-lookup"><span data-stu-id="8915b-137">Response</span></span>

<span data-ttu-id="8915b-p104">В случае успешного выполнения этот метод возвращает код отклика `200 OK`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="8915b-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8915b-140">Пример</span><span class="sxs-lookup"><span data-stu-id="8915b-140">Example</span></span>
<span data-ttu-id="8915b-141">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="8915b-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="8915b-142">Запрос</span><span class="sxs-lookup"><span data-stu-id="8915b-142">Request</span></span>
<span data-ttu-id="8915b-143">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="8915b-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_snoozereminder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/snoozeReminder
Content-type: application/json
Content-length: 97

{
  "newReminderTime": {
    "dateTime": "dateTime-value",
    "timeZone": "timeZone-value"
  }
}
```

##### <a name="response"></a><span data-ttu-id="8915b-144">Отклик</span><span class="sxs-lookup"><span data-stu-id="8915b-144">Response</span></span>
<span data-ttu-id="8915b-145">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="8915b-145">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event: snoozeReminder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
