# <a name="reminder-resource-type"></a><span data-ttu-id="4e6a2-101">Тип ресурса reminder</span><span class="sxs-lookup"><span data-stu-id="4e6a2-101">reminder resource type</span></span>

<span data-ttu-id="4e6a2-102">Напоминание для [события](event.md) из [календаря](calendar.md)пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-102">A reminder for an [event](event.md) in a user [calendar](calendar.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4e6a2-103">Свойства</span><span class="sxs-lookup"><span data-stu-id="4e6a2-103">Properties</span></span>
| <span data-ttu-id="4e6a2-104">Свойство</span><span class="sxs-lookup"><span data-stu-id="4e6a2-104">Property</span></span>     | <span data-ttu-id="4e6a2-105">Тип</span><span class="sxs-lookup"><span data-stu-id="4e6a2-105">Type</span></span>   |<span data-ttu-id="4e6a2-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4e6a2-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4e6a2-107">changeKey</span><span class="sxs-lookup"><span data-stu-id="4e6a2-107">changeKey</span></span>|<span data-ttu-id="4e6a2-108">String (строка)</span><span class="sxs-lookup"><span data-stu-id="4e6a2-108">String</span></span>|<span data-ttu-id="4e6a2-p101">Указывает версию напоминания. При каждом изменении напоминания также меняется значение **changeKey**. Благодаря этому Exchange может применять изменения к правильной версии объекта.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-p101">Identifies the version of the reminder. Every time the reminder is changed, **changeKey** changes as well. This allows Exchange to apply changes to the correct version of the object.</span></span>|
|<span data-ttu-id="4e6a2-112">eventEndTime</span><span class="sxs-lookup"><span data-stu-id="4e6a2-112">eventEndTime</span></span>|[<span data-ttu-id="4e6a2-113">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="4e6a2-113">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="4e6a2-114">Дата, время и часовой пояс завершения события.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-114">The date, time and time zone that the event ends.</span></span>|
|<span data-ttu-id="4e6a2-115">eventId</span><span class="sxs-lookup"><span data-stu-id="4e6a2-115">eventId</span></span>|<span data-ttu-id="4e6a2-116">String (строка)</span><span class="sxs-lookup"><span data-stu-id="4e6a2-116">String</span></span>|<span data-ttu-id="4e6a2-p102">Уникальный идентификатор события. Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-p102">The unique ID of the event. Read only.</span></span>|
|<span data-ttu-id="4e6a2-119">eventLocation</span><span class="sxs-lookup"><span data-stu-id="4e6a2-119">eventLocation</span></span>|[<span data-ttu-id="4e6a2-120">Location</span><span class="sxs-lookup"><span data-stu-id="4e6a2-120">Location</span></span>](location.md)|<span data-ttu-id="4e6a2-121">Место проведения события.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-121">The location of the event.</span></span>|
|<span data-ttu-id="4e6a2-122">eventStartTime</span><span class="sxs-lookup"><span data-stu-id="4e6a2-122">eventStartTime</span></span>|[<span data-ttu-id="4e6a2-123">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="4e6a2-123">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="4e6a2-124">Дата, время и часовой пояс начала события.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-124">The date, time, and time zone that the event starts.</span></span>|
|<span data-ttu-id="4e6a2-125">eventSubject</span><span class="sxs-lookup"><span data-stu-id="4e6a2-125">eventSubject</span></span>|<span data-ttu-id="4e6a2-126">String (строка)</span><span class="sxs-lookup"><span data-stu-id="4e6a2-126">String</span></span>|<span data-ttu-id="4e6a2-127">Текст в строке темы события.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-127">The text of the event's subject line.</span></span>|
|<span data-ttu-id="4e6a2-128">eventWebLink</span><span class="sxs-lookup"><span data-stu-id="4e6a2-128">eventWebLink</span></span>|<span data-ttu-id="4e6a2-129">String (строка)</span><span class="sxs-lookup"><span data-stu-id="4e6a2-129">String</span></span>|<span data-ttu-id="4e6a2-130">URL-адрес для открытия события в Outlook в Интернете.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-130">The URL to open the event in Outlook on the web.</span></span><br/><br/><span data-ttu-id="4e6a2-p103">Событие откроется в браузере, если вы вошли в свой почтовый ящик с помощью Outlook в Интернете. Если вход с помощью браузера еще не выполнен, вам будет предложено войти.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-p103">The event will open in the browser if you are logged in to your mailbox via Outlook on the web. You will be prompted to login if you are not already logged in with the browser.</span></span><br/><br/><span data-ttu-id="4e6a2-133">Доступ к этому URL-адресу можно получить из объекта iFrame.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-133">This URL can be accessed from within an iFrame.</span></span>|
|<span data-ttu-id="4e6a2-134">reminderFireTime</span><span class="sxs-lookup"><span data-stu-id="4e6a2-134">reminderFireTime</span></span>|[<span data-ttu-id="4e6a2-135">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="4e6a2-135">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="4e6a2-136">Дата, время и часовой пояс, заданные для упоминания.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-136">The date, time, and time zone that the reminder is set to occur.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4e6a2-137">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="4e6a2-137">JSON representation</span></span>

<span data-ttu-id="4e6a2-138">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="4e6a2-138">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.reminder"
}-->

```json
{
  "changeKey": "string",
  "eventEndTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "eventId": "string",
  "eventLocation": {"@odata.type": "microsoft.graph.location"},
  "eventStartTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "eventSubject": "string",
  "eventWebLink": "string",
  "reminderFireTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "reminder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->