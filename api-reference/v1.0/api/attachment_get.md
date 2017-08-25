# <a name="get-attachment"></a><span data-ttu-id="4eccb-101">Вывод вложения</span><span class="sxs-lookup"><span data-stu-id="4eccb-101">Get attachment</span></span>

<span data-ttu-id="4eccb-102">Чтение свойств и связей объекта, представляющего вложение, которое было добавлено к [данным о событии](../resources/event.md), [сообщению](../resources/message.md) или [записи](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="4eccb-102">Read the properties and relationships of an attachment, attached to an [event](../resources/event.md), [message](../resources/message.md), or [post](../resources/post.md).</span></span> 

<span data-ttu-id="4eccb-103">Допустимые типы вложений:</span><span class="sxs-lookup"><span data-stu-id="4eccb-103">An attachment can be one of the following types:</span></span>

* <span data-ttu-id="4eccb-104">файл (ресурс [fileAttachment](../resources/fileattachment.md));</span><span class="sxs-lookup"><span data-stu-id="4eccb-104">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="4eccb-p101">элемент (контакт, событие или сообщение, представленные ресурсом [itemAttachment](../resources/itemattachment.md)); Вы можете использовать `$expand` для получения других свойств этого элемента. См. [пример](#request-2) ниже.</span><span class="sxs-lookup"><span data-stu-id="4eccb-p101">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource). You can use `$expand` to further get the properties of that item. See an [example](#request-2) below.</span></span>
* <span data-ttu-id="4eccb-108">ссылка на файл (ресурс [referenceAttachment](../resources/referenceAttachment.md)).</span><span class="sxs-lookup"><span data-stu-id="4eccb-108">A link to a file ([referenceAttachment](../resources/referenceAttachment.md) resource).</span></span>

<span data-ttu-id="4eccb-109">Все эти типы ресурсов вложений являются производными от ресурса [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="4eccb-109">All these types of attachment resources are derived from the [attachment](../resources/attachment.md) resource.</span></span> 


## <a name="permissions"></a><span data-ttu-id="4eccb-110">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4eccb-110">Permissions</span></span>
<span data-ttu-id="4eccb-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4eccb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

* <span data-ttu-id="4eccb-113">При доступе к вложениям в сообщениях: Mail.Read.</span><span class="sxs-lookup"><span data-stu-id="4eccb-113">If accessing attachments in messages: Mail.Read</span></span>
* <span data-ttu-id="4eccb-114">При доступе к вложениям в данных о событиях: Calendars.Read.</span><span class="sxs-lookup"><span data-stu-id="4eccb-114">If accessing attachments in events: Calendars.Read</span></span>
* <span data-ttu-id="4eccb-115">При доступе к вложениям в записях или данных о событиях групп: Group.Read.All.</span><span class="sxs-lookup"><span data-stu-id="4eccb-115">If accessing attachments in group events or posts: Group.Read.All</span></span>

## <a name="http-request"></a><span data-ttu-id="4eccb-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="4eccb-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="4eccb-117">Вложения [события](../resources/event.md) в [календаре](../resources/calendar.md) по умолчанию для пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="4eccb-117">Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
GET /me/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/events/{id}/attachments/{id}
GET /groups/{id}/events/{id}/attachments/{id}

GET /me/calendar/{id}/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/calendar/events/{id}/attachments/{id}
GET /groups/{id}/calendar/events/{id}/attachments/{id}
```
<span data-ttu-id="4eccb-118">Вложения [события](../resources/event.md) в [календаре](../resources/calendar.md), принадлежащем к группе [calendarGroup](../resources/calendargroup.md) по умолчанию для пользователя.</span><span class="sxs-lookup"><span data-stu-id="4eccb-118">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendars/{id}/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments/{id}

GET /me/calendargroup/calendars/{id}/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="4eccb-119">Вложения [события](../resources/event.md) в [календаре](../resources/calendar.md), принадлежащем к группе [calendarGroup](../resources/calendargroup.md) пользователя.</span><span class="sxs-lookup"><span data-stu-id="4eccb-119">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="4eccb-120">Вложения [сообщения](../resources/message.md) в почтовом ящике пользователя.</span><span class="sxs-lookup"><span data-stu-id="4eccb-120">Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
```http
GET /me/messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/messages/{id}/attachments/{id}
```
<span data-ttu-id="4eccb-121">Вложения [сообщения](../resources/message.md) в папке [mailFolder](../resources/mailfolder.md) верхнего уровня в почтовом ящике пользователя.</span><span class="sxs-lookup"><span data-stu-id="4eccb-121">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
```http
GET /me/mailFolders/{id}/messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="4eccb-p103">Вложения [сообщения](../resources/message.md) в дочерней папке объекта [mailFolder](../resources/mailfolder.md) в почтовом ящике пользователя.  В приведенном ниже примере показан один уровень вложенности, но сообщение может находиться в папке, вложенной в дочернюю, и т. д.</span><span class="sxs-lookup"><span data-stu-id="4eccb-p103">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.  The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
```http
GET /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="4eccb-124">Вложения для [записи](../resources/post.md) в [цепочке](../resources/conversationthread.md) [беседы](../resources/conversation.md) в группе.</span><span class="sxs-lookup"><span data-stu-id="4eccb-124">Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
```http
GET /groups/{id}/threads/{id}/posts/{id}/attachments/{id}
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4eccb-125">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="4eccb-125">Optional query parameters</span></span>
<span data-ttu-id="4eccb-126">Этот метод поддерживает [параметры запросов OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="4eccb-126">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="4eccb-127">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="4eccb-127">Request headers</span></span>
| <span data-ttu-id="4eccb-128">Имя</span><span class="sxs-lookup"><span data-stu-id="4eccb-128">Name</span></span>       | <span data-ttu-id="4eccb-129">Тип</span><span class="sxs-lookup"><span data-stu-id="4eccb-129">Type</span></span> | <span data-ttu-id="4eccb-130">Описание</span><span class="sxs-lookup"><span data-stu-id="4eccb-130">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="4eccb-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="4eccb-131">Authorization</span></span>  | <span data-ttu-id="4eccb-132">string</span><span class="sxs-lookup"><span data-stu-id="4eccb-132">string</span></span>  | <span data-ttu-id="4eccb-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4eccb-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4eccb-135">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="4eccb-135">Request body</span></span>
<span data-ttu-id="4eccb-136">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="4eccb-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4eccb-137">Отклик</span><span class="sxs-lookup"><span data-stu-id="4eccb-137">Response</span></span>

<span data-ttu-id="4eccb-p105">В случае успеха этот метод возвращает код ответа `200 OK` и объект **attachment** в тексте ответа. Кроме того, возвращаются свойства этого типа вложения: [fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md) или [referenceAttachment](../resources/referenceAttachment.md).</span><span class="sxs-lookup"><span data-stu-id="4eccb-p105">If successful, this method returns a `200 OK` response code and an **attachment** object in the response body. The properties of that type of attachment are returned: [fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md), or [referenceAttachment](../resources/referenceAttachment.md).</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="4eccb-140">Пример (вложенный файл)</span><span class="sxs-lookup"><span data-stu-id="4eccb-140">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="4eccb-141">Запрос</span><span class="sxs-lookup"><span data-stu-id="4eccb-141">Request</span></span>
<span data-ttu-id="4eccb-142">Ниже приведен пример запроса на получение вложенного файла из данных, касающихся события.</span><span class="sxs-lookup"><span data-stu-id="4eccb-142">Here is an example of the request to get a file attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_file_attachment"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/{id}/attachments/{id}
```

##### <a name="response"></a><span data-ttu-id="4eccb-143">Отклик</span><span class="sxs-lookup"><span data-stu-id="4eccb-143">Response</span></span>
<span data-ttu-id="4eccb-p106">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="4eccb-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.fileAttachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 199

{
  "@odata.type": "#microsoft.graph.fileAttachment",
  "contentType": "contentType-value",
  "contentLocation": "contentLocation-value",
  "contentBytes": "contentBytes-value",
  "contentId": "null",
  "lastModifiedDateTime": "2016-01-01T12:00:00Z",
  "id": "id-value",
  "isInline": false,
  "name": "name-value",
  "size": 99
}
```
## <a name="example-item-attachment"></a><span data-ttu-id="4eccb-147">Пример (вложенный элемент)</span><span class="sxs-lookup"><span data-stu-id="4eccb-147">Example (item attachment)</span></span>

##### <a name="request-1"></a><span data-ttu-id="4eccb-148">Запрос 1</span><span class="sxs-lookup"><span data-stu-id="4eccb-148">Request 1</span></span>
<span data-ttu-id="4eccb-p107">В первом примере показано, как получить вложенный элемент в сообщении. Возвращаются свойства **itemAttachment**.</span><span class="sxs-lookup"><span data-stu-id="4eccb-p107">The first example shows how to get an item attachment on a message. The properties of the **itemAttachment** are returned.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_item_attachment"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages('AAMkADA1M-zAAA=')/attachments('AAMkADA1M-CJKtzmnlcqVgqI=')
```

##### <a name="response-1"></a><span data-ttu-id="4eccb-151">Отклик 1</span><span class="sxs-lookup"><span data-stu-id="4eccb-151">Response 1</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.itemAttachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/messages('AAMkADA1M-zAAA%3D')/attachments/$entity",
  "@odata.type":"#microsoft.graph.itemAttachment",
  "id":"AAMkADA1MCJKtzmnlcqVgqI=",
  "lastModifiedDateTime":"2017-07-21T00:20:34Z",
  "name":"Reminder - please bring laptop",
  "contentType":null,
  "size":32005,
  "isInline":false
}
```

##### <a name="request-2"></a><span data-ttu-id="4eccb-152">Запрос 2</span><span class="sxs-lookup"><span data-stu-id="4eccb-152">Request 2</span></span>
<span data-ttu-id="4eccb-p108">В следующем примере показано, как использовать `$expand` для получения свойств элемента, вложенного в сообщение. В этом примере вложением является сообщением. Свойства вложенного сообщения также возвращаются.</span><span class="sxs-lookup"><span data-stu-id="4eccb-p108">The next example shows how to use `$expand` to get the properties of the item that is attached to the message. In this example, that item is a message; the properties of that attached message are also returned.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_and_expand_item_attachment"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages('AAMkADA1M-zAAA=')/attachments('AAMkADA1M-CJKtzmnlcqVgqI=')/?$expand=microsoft.graph.itemattachment/item 
```

##### <a name="response-2"></a><span data-ttu-id="4eccb-155">Отклик 2</span><span class="sxs-lookup"><span data-stu-id="4eccb-155">Response 2</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.itemAttachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/messages('AAMkADA1M-zAAA%3D')/attachments/$entity",
  "@odata.type":"#microsoft.graph.itemAttachment",
  "id":"AAMkADA1MCJKtzmnlcqVgqI=",
  "lastModifiedDateTime":"2017-07-21T00:20:34Z",
  "name":"Reminder - please bring laptop",
  "contentType":null,
  "size":32005,
  "isInline":false,
  "item@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/messages('AAMkADA1M-zAAA%3D')/attachments('AAMkADA1M-CJKtzmnlcqVgqI%3D')/microsoft.graph.itemAttachment/item/$entity",
  "item":{
    "@odata.type":"#microsoft.graph.message",
    "id":"",
    "createdDateTime":"2017-07-21T00:20:41Z",
    "lastModifiedDateTime":"2017-07-21T00:20:34Z",
    "receivedDateTime":"2017-07-21T00:19:55Z",
    "sentDateTime":"2017-07-21T00:19:52Z",
    "hasAttachments":false,
    "internetMessageId":"<BY2PR15MB05189A084C01F466709E414F9CA40@BY2PR15MB0518.namprd15.prod.outlook.com>",
    "subject":"Reminder - please bring laptop",
    "importance":"normal",
    "conversationId":"AAQkADA1MzMyOGI4LTlkZDctNDkzYy05M2RiLTdiN2E1NDE3MTRkOQAQAMG_NSCMBqdKrLa2EmR-lO0=",
    "isDeliveryReceiptRequested":false,
    "isReadReceiptRequested":false,
    "isRead":false,
    "isDraft":false,
    "webLink":"https://outlook.office365.com/owa/?ItemID=AAMkADA1M3MTRkOQAAAA%3D%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "body":{
      "contentType":"html",
      "content":"<html><head>\r\n</head>\r\n<body>\r\n</body>\r\n</html>"
    },
    "sender":{
      "emailAddress":{
        "name":"Adele Vance",
        "address":"AdeleV@contoso.onmicrosoft.com"
      }
    },
    "from":{
      "emailAddress":{
        "name":"Adele Vance",
        "address":"AdeleV@contoso.onmicrosoft.com"
      }
    },
    "toRecipients":[
      {
        "emailAddress":{
          "name":"Alex Wilbur",
          "address":"AlexW@contoso.onmicrosoft.com"
        }
      }
    ],
    "ccRecipients":[
      {
        "emailAddress":{
          "name":"Adele Vance",
          "address":"AdeleV@contoso.onmicrosoft.com"
        }
      }
    ]
  }
}
```



## <a name="example-reference-attachment"></a><span data-ttu-id="4eccb-156">Пример (вложенная ссылка)</span><span class="sxs-lookup"><span data-stu-id="4eccb-156">Example (reference attachment)</span></span>
##### <a name="request"></a><span data-ttu-id="4eccb-157">Запрос</span><span class="sxs-lookup"><span data-stu-id="4eccb-157">Request</span></span>
<span data-ttu-id="4eccb-158">Ниже приведен пример запроса на получение вложенной ссылки из данных, касающихся события.</span><span class="sxs-lookup"><span data-stu-id="4eccb-158">Here is an example of the request to get a reference attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_reference_attachment"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/{id}/attachments/{id}
```
##### <a name="response"></a><span data-ttu-id="4eccb-159">Отклик</span><span class="sxs-lookup"><span data-stu-id="4eccb-159">Response</span></span>
<span data-ttu-id="4eccb-p109">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="4eccb-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.referenceAttachment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "@odata.type": "#microsoft.graph.referenceAttachment",
  "contentType": "contentType-value",
  "lastModifiedDateTime": "datetime-value",
  "id": "id-value",
  "isInline": false,
  "name": "name-value",
  "size": 99,
}
```



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get attachment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
