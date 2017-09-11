# <a name="get-event"></a><span data-ttu-id="16bdf-101">Получение события</span><span class="sxs-lookup"><span data-stu-id="16bdf-101">Get event</span></span>

<span data-ttu-id="16bdf-102">Получение свойств и отношений указанного объекта [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="16bdf-102">Get the properties and relationships of the specified [event](../resources/event.md) object.</span></span>

<span data-ttu-id="16bdf-103">В настоящее время эта операция возвращает текст события только в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="16bdf-103">Currently, this operation returns event bodies in only HTML format.</span></span>

<span data-ttu-id="16bdf-104">Так как ресурс **event** поддерживает [расширения](../../../concepts/extensibility_overview.md), с помощью операции `GET` можно получить настраиваемые свойства и данные расширения в экземпляре **event**.</span><span class="sxs-lookup"><span data-stu-id="16bdf-104">Since the **event** resource supports [extensions](../../../concepts/extensibility_overview.md), you can also use the `GET` operation to get custom properties and extension data in an **event** instance.</span></span>

### <a name="support-various-time-zones"></a><span data-ttu-id="16bdf-105">Поддержка разных часовых поясов</span><span class="sxs-lookup"><span data-stu-id="16bdf-105">Support various time zones</span></span>

<span data-ttu-id="16bdf-106">Для всех операций GET, которые возвращают события, можно использовать заголовок `Prefer: outlook.timezone`, чтобы задать часовой пояс для указанного в отклике времени начала и завершения события.</span><span class="sxs-lookup"><span data-stu-id="16bdf-106">For all GET operations that return events, you can use the `Prefer: outlook.timezone` header to specify the time zone for the event start and end times in the response.</span></span> 

<span data-ttu-id="16bdf-107">Например, заголовок `Prefer: outlook.timezone` задает в отклике время начала и завершения согласно североамериканскому восточному времени.</span><span class="sxs-lookup"><span data-stu-id="16bdf-107">For example, the following `Prefer: outlook.timezone` header sets the start and end times in the response to Eastern Standard Time.</span></span>
```http
Prefer: outlook.timezone="Eastern Standard Time"
```

<span data-ttu-id="16bdf-p101">Если событие создано с применением другого часового пояса, время начала и завершения будет изменено в соответствии с часовым поясом, указанным в заголовке `Prefer`. Поддерживаемые часовые пояса указаны в этом [списке](../resources/datetimetimezone.md). Если заголовок `Prefer: outlook.timezone` не указан, время начала и завершения возвращается в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="16bdf-p101">If the event was created in a different time zone, the start and end times will be adjusted to the time zone specified in that `Prefer` header. See this [list](../resources/datetimetimezone.md) for the supported time zone names. If the `Prefer: outlook.timezone` header is not specified, the start and end times are returned in UTC.</span></span>

<span data-ttu-id="16bdf-111">Узнать, какой именно часовой пояс использовался при создании события, позволят свойства **OriginalStartTimeZone** и **OriginalEndTimeZone** ресурса **event**.</span><span class="sxs-lookup"><span data-stu-id="16bdf-111">You can use the **OriginalStartTimeZone** and **OriginalEndTimeZone** properties on the **event** resource to find out the time zone used when the event was created.</span></span>


## <a name="permissions"></a><span data-ttu-id="16bdf-112">Разрешения</span><span class="sxs-lookup"><span data-stu-id="16bdf-112">Permissions</span></span>
<span data-ttu-id="16bdf-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="16bdf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="16bdf-115">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="16bdf-115">Permission type</span></span>      | <span data-ttu-id="16bdf-116">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="16bdf-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="16bdf-117">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="16bdf-117">Delegated (work or school account)</span></span> | <span data-ttu-id="16bdf-118">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="16bdf-118">Calendars.Read</span></span>    |
|<span data-ttu-id="16bdf-119">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="16bdf-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="16bdf-120">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="16bdf-120">Calendars.Read</span></span>    |
|<span data-ttu-id="16bdf-121">Для приложений</span><span class="sxs-lookup"><span data-stu-id="16bdf-121">Application</span></span> | <span data-ttu-id="16bdf-122">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="16bdf-122">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="16bdf-123">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="16bdf-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}
GET /users/{id | userPrincipalName}/events/{id}
GET /groups/{id}/events/{id}

GET /me/calendar/events/{id}
GET /users/{id | userPrincipalName}/calendar/events/{id}
GET /groups/{id}/calendar/events/{id}

GET /me/calendars/{id}/events/{id}
GET /users/{id | userPrincipalName}/calendars/{id}/events/{id}

GET /me/calendargroup/calendars/{id}/events/{id}
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}

GET /me/calendargroups/{id}/calendars/{id}/events/{id}
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="16bdf-124">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="16bdf-124">Optional query parameters</span></span>
<span data-ttu-id="16bdf-125">Этот метод поддерживает [параметры запросов OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="16bdf-125">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="16bdf-126">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="16bdf-126">Request headers</span></span>
| <span data-ttu-id="16bdf-127">Имя</span><span class="sxs-lookup"><span data-stu-id="16bdf-127">Name</span></span>       | <span data-ttu-id="16bdf-128">Тип</span><span class="sxs-lookup"><span data-stu-id="16bdf-128">Type</span></span> | <span data-ttu-id="16bdf-129">Описание</span><span class="sxs-lookup"><span data-stu-id="16bdf-129">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="16bdf-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="16bdf-130">Authorization</span></span>  | <span data-ttu-id="16bdf-131">string</span><span class="sxs-lookup"><span data-stu-id="16bdf-131">string</span></span>  | <span data-ttu-id="16bdf-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="16bdf-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="16bdf-134">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="16bdf-134">Prefer: outlook.timezone</span></span> | <span data-ttu-id="16bdf-135">string</span><span class="sxs-lookup"><span data-stu-id="16bdf-135">string</span></span> | <span data-ttu-id="16bdf-136">Часовой пояс по умолчанию для событий, указанных в отклике.</span><span class="sxs-lookup"><span data-stu-id="16bdf-136">The default time zone for events in the response.</span></span> |

## <a name="request-body"></a><span data-ttu-id="16bdf-137">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="16bdf-137">Request body</span></span>
<span data-ttu-id="16bdf-138">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="16bdf-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="16bdf-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="16bdf-139">Response</span></span>

<span data-ttu-id="16bdf-140">В случае успеха этот метод возвратит код отклика `200 OK` и объект [event](../resources/event.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="16bdf-140">If successful, this method returns a `200 OK` response code and [event](../resources/event.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="16bdf-141">Пример</span><span class="sxs-lookup"><span data-stu-id="16bdf-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="16bdf-142">Запрос</span><span class="sxs-lookup"><span data-stu-id="16bdf-142">Request</span></span>
<span data-ttu-id="16bdf-p104">Первый пример возвращает указанное событие. Он указывает следующее:</span><span class="sxs-lookup"><span data-stu-id="16bdf-p104">The first example gets the specified event. It specifies the following:</span></span>

- <span data-ttu-id="16bdf-145">Заголовок `Prefer: outlook.timezone` для получения значений даты и времени, которые возвращаются для стандартного тихоокеанского времени.</span><span class="sxs-lookup"><span data-stu-id="16bdf-145">A `Prefer: outlook.timezone` header to get date time values returned in Pacific Standard Time.</span></span> 
- <span data-ttu-id="16bdf-p105">Параметр запроса `$select`, который возвращает конкретные свойства. Без параметра `$select` будут возвращены все свойства событий.</span><span class="sxs-lookup"><span data-stu-id="16bdf-p105">A `$select` query parameter to return specific properties. Without a `$select` parameter, all of the event properties will be returned.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_event"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/events('AAMkAGIAAAoZDOFAAA=')?$select=subject,body,bodyPreview,organizer,attendees,start,end,location 
Prefer: outlook.timezone="Pacific Standard Time"
```

##### <a name="response"></a><span data-ttu-id="16bdf-148">Отклик</span><span class="sxs-lookup"><span data-stu-id="16bdf-148">Response</span></span>

<span data-ttu-id="16bdf-p106">Ниже приведен пример отклика. Свойство **body** возвращается в формате HTML по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16bdf-p106">Here is an example of the response. The **body** property is returned in the default format of HTML.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Preference-Applied: outlook.timezone="Pacific Standard Time"
Content-length: 1928

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/events(subject,body,bodyPreview,organizer,attendees,start,end,location)/$entity",
    "@odata.etag":"W/\"ZlnW4RIAV06KYYwlrfNZvQAAKGWwbw==\"",
    "id":"AAMkAGIAAAoZDOFAAA=",
    "subject":"Orientation ",
    "bodyPreview":"Dana, this is the time you selected for our orientation. Please bring the notes I sent you.",
    "body":{
        "contentType":"html",
        "content":"<html><head></head><body><p>Dana, this is the time you selected for our orientation. Please bring the notes I sent you.</p></body></html>"
    },
    "start":{
        "dateTime":"2017-04-21T10:00:00.0000000",
        "timeZone":"Pacific Standard Time"
    },
    "end":{
        "dateTime":"2017-04-21T12:00:00.0000000",
        "timeZone":"Pacific Standard Time"
    },
    "location":{
        "displayName":"Assembly Hall"
    },
    "attendees":[
        {
            "type":"required",
            "status":{
                "response":"none",
                "time":"0001-01-01T00:00:00Z"
            },
            "emailAddress":{
                "name":"Samantha Booth",
                "address":"samanthab@a830edad905084922E17020313.onmicrosoft.com"
            }
        },
        {
            "type":"required",
            "status":{
                "response":"none",
                "time":"0001-01-01T00:00:00Z"
            },
            "emailAddress":{
                "name":"Dana Swope",
                "address":"danas@a830edad905084922E17020313.onmicrosoft.com"
            }
        }
    ],
    "organizer":{
        "emailAddress":{
            "name":"Samantha Booth",
            "address":"samanthab@a830edad905084922E17020313.onmicrosoft.com"
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="16bdf-151">См. также</span><span class="sxs-lookup"><span data-stu-id="16bdf-151">See also</span></span>

- [<span data-ttu-id="16bdf-152">Добавление пользовательских данных в ресурсы с помощью расширений</span><span class="sxs-lookup"><span data-stu-id="16bdf-152">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="16bdf-153">Добавление пользовательских данных в ресурсы user с помощью открытых расширений (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="16bdf-153">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
<!--
- [Add custom data to groups using schema extensions (preview)](../../../concepts/extensibility_schema_groups.md)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
