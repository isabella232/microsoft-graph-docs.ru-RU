---
title: Обновление календаря
description: 'Обновление свойств объекта calendar. Календарь может быть одним для пользователя, '
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: ad372b18397d24185c3e05daabe206fc3336f544
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32580589"
---
# <a name="update-calendar"></a><span data-ttu-id="e42eb-104">Обновление календаря</span><span class="sxs-lookup"><span data-stu-id="e42eb-104">Update calendar</span></span>

<span data-ttu-id="e42eb-105">Обновление свойств объекта [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="e42eb-105">Update the properties of of a [calendar](../resources/calendar.md) object.</span></span> <span data-ttu-id="e42eb-106">Это может быть календарь для ресурса [user](../resources/user.md) или стандартный календарь для ресурса [group](../resources/group.md), представляющего группу Office 365.</span><span class="sxs-lookup"><span data-stu-id="e42eb-106">The calendar can be one for a [user](../resources/user.md), or the default calendar of an Office 365 [group](../resources/group.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="e42eb-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="e42eb-107">Permissions</span></span>
<span data-ttu-id="e42eb-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e42eb-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e42eb-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="e42eb-110">Permission type</span></span>      | <span data-ttu-id="e42eb-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="e42eb-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e42eb-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="e42eb-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e42eb-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e42eb-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="e42eb-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="e42eb-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e42eb-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e42eb-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="e42eb-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="e42eb-116">Application</span></span> | <span data-ttu-id="e42eb-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e42eb-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="e42eb-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="e42eb-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="e42eb-119">[Календарь](../resources/calendar.md) пользователя или группы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e42eb-119">A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
PATCH /me/calendar
PATCH /users/{id | userPrincipalName}/calendar
PATCH /groups/{id}/calendar
```
<span data-ttu-id="e42eb-120">Экземпляр [calendar](../resources/calendar.md) пользователя в экземпляре по умолчанию [calendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="e42eb-120">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
PATCH /me/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendars/{id}

PATCH /me/calendarGroup/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="e42eb-121">[Календарь](../resources/calendar.md) пользователя в определенной группе [calendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="e42eb-121">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
PATCH /me/calendarGroups/{id}/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="request-headers"></a><span data-ttu-id="e42eb-122">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="e42eb-122">Request headers</span></span>
| <span data-ttu-id="e42eb-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e42eb-123">Header</span></span>       | <span data-ttu-id="e42eb-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e42eb-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e42eb-125">Авторизация</span><span class="sxs-lookup"><span data-stu-id="e42eb-125">Authorization</span></span>  | <span data-ttu-id="e42eb-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e42eb-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="e42eb-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e42eb-128">Content-Type</span></span>  | <span data-ttu-id="e42eb-p105">application/json. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e42eb-p105">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e42eb-131">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="e42eb-131">Request body</span></span>
<span data-ttu-id="e42eb-p106">В тексте запроса укажите значения для соответствующих полей, которые необходимо обновить. Предыдущие значения существующих свойств, не включенных в текст запроса, останутся прежними или будут повторно вычислены с учетом измененных значений других свойств. Для достижения оптимальной производительности не следует включать существующие значения, которые не изменились.</span><span class="sxs-lookup"><span data-stu-id="e42eb-p106">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="e42eb-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="e42eb-135">Property</span></span>     | <span data-ttu-id="e42eb-136">Тип</span><span class="sxs-lookup"><span data-stu-id="e42eb-136">Type</span></span>   |<span data-ttu-id="e42eb-137">Описание</span><span class="sxs-lookup"><span data-stu-id="e42eb-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e42eb-138">color</span><span class="sxs-lookup"><span data-stu-id="e42eb-138">color</span></span>|<span data-ttu-id="e42eb-139">String</span><span class="sxs-lookup"><span data-stu-id="e42eb-139">String</span></span>|<span data-ttu-id="e42eb-p107">Задает цветовую тему, отличающую этот календарь от других календарей в пользовательском интерфейсе. Значения свойств: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1</span><span class="sxs-lookup"><span data-stu-id="e42eb-p107">Specifies the color theme to distinguish the calendar from other calendars in a UI. The property values are: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1</span></span>|
|<span data-ttu-id="e42eb-142">name</span><span class="sxs-lookup"><span data-stu-id="e42eb-142">name</span></span>|<span data-ttu-id="e42eb-143">String</span><span class="sxs-lookup"><span data-stu-id="e42eb-143">String</span></span>|<span data-ttu-id="e42eb-144">Имя календаря.</span><span class="sxs-lookup"><span data-stu-id="e42eb-144">The calendar name.</span></span>|

## <a name="response"></a><span data-ttu-id="e42eb-145">Отклик</span><span class="sxs-lookup"><span data-stu-id="e42eb-145">Response</span></span>

<span data-ttu-id="e42eb-146">В случае успеха этот метод возвратит код отклика `200 OK` и обновленный объект [calendar](../resources/calendar.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="e42eb-146">If successful, this method returns a `200 OK` response code and updated [calendar](../resources/calendar.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e42eb-147">Пример</span><span class="sxs-lookup"><span data-stu-id="e42eb-147">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e42eb-148">Запрос</span><span class="sxs-lookup"><span data-stu-id="e42eb-148">Request</span></span>
<span data-ttu-id="e42eb-149">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="e42eb-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_calendar"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/calendar
Content-type: application/json

{
  "name": "Social events"
}
```
##### <a name="response"></a><span data-ttu-id="e42eb-150">Отклик</span><span class="sxs-lookup"><span data-stu-id="e42eb-150">Response</span></span>
<span data-ttu-id="e42eb-p108">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="e42eb-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#me/calendars/$entity",
    "@odata.id":"https://graph.microsoft.com/v1.0/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/calendars('AAMkADJmMVAAA=')",
    "id":"AAMkADJmMVAAA=",
    "name":"Social events",
    "color":"auto",
    "changeKey":"DxYSthXJXEWwAQSYQnXvIgAAIxGttg==",
    "canShare":true,
    "canViewPrivateItems":true,
    "canEdit":true,
    "owner":{
        "name":"Samantha Booth",
        "address":"samanthab@adatum.onmicrosoft.com"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
