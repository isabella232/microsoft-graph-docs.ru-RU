# <a name="fileattachment-resource-type"></a><span data-ttu-id="30a74-101">Тип ресурса fileAttachment</span><span class="sxs-lookup"><span data-stu-id="30a74-101">fileAttachment resource type</span></span>

<span data-ttu-id="30a74-p101">Файл (например, текстовый файл или документ Word), вложенный в сведения о событии, сообщение или запись. Свойство **contentBytes** включает содержимое файла в кодировке Base 64.</span><span class="sxs-lookup"><span data-stu-id="30a74-p101">A file (such as a text file or Word document) attached to an event, message or post. The  **contentBytes** property contains the base64-encoded contents of the file.</span></span>  

<span data-ttu-id="30a74-104">При создании вложенного файла включите в текст запроса следующее:</span><span class="sxs-lookup"><span data-stu-id="30a74-104">When creating a file attachment, include the following in the request body:</span></span>

* `"@odata.type": "#microsoft.graph.fileAttachment"`
* <span data-ttu-id="30a74-105">Обязательные свойства **name** и **contentBytes**.</span><span class="sxs-lookup"><span data-stu-id="30a74-105">The required properties **name** and **contentBytes**.</span></span>

<span data-ttu-id="30a74-106">Производный от типа [attachment](attachment.md).</span><span class="sxs-lookup"><span data-stu-id="30a74-106">Derived from [attachment](attachment.md).</span></span>

## <a name="methods"></a><span data-ttu-id="30a74-107">Методы</span><span class="sxs-lookup"><span data-stu-id="30a74-107">Methods</span></span>

| <span data-ttu-id="30a74-108">Метод</span><span class="sxs-lookup"><span data-stu-id="30a74-108">Method</span></span>       | <span data-ttu-id="30a74-109">Возвращаемый тип</span><span class="sxs-lookup"><span data-stu-id="30a74-109">Return Type</span></span>  |<span data-ttu-id="30a74-110">Описание</span><span class="sxs-lookup"><span data-stu-id="30a74-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="30a74-111">Получение</span><span class="sxs-lookup"><span data-stu-id="30a74-111">Get</span></span>](../api/attachment_get.md) | [<span data-ttu-id="30a74-112">fileAttachment</span><span class="sxs-lookup"><span data-stu-id="30a74-112">fileAttachment</span></span>](fileattachment.md) |<span data-ttu-id="30a74-113">Чтение свойств и связей объекта fileAttachment.</span><span class="sxs-lookup"><span data-stu-id="30a74-113">Read properties and relationships of fileAttachment object.</span></span>|
|[<span data-ttu-id="30a74-114">Удаление</span><span class="sxs-lookup"><span data-stu-id="30a74-114">Delete</span></span>](../api/attachment_delete.md) | <span data-ttu-id="30a74-115">Нет</span><span class="sxs-lookup"><span data-stu-id="30a74-115">None</span></span> |<span data-ttu-id="30a74-116">Удаление объекта fileAttachment.</span><span class="sxs-lookup"><span data-stu-id="30a74-116">Delete fileAttachment object.</span></span> |

## <a name="properties"></a><span data-ttu-id="30a74-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="30a74-117">Properties</span></span>
| <span data-ttu-id="30a74-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="30a74-118">Property</span></span>     | <span data-ttu-id="30a74-119">Тип</span><span class="sxs-lookup"><span data-stu-id="30a74-119">Type</span></span>   |<span data-ttu-id="30a74-120">Описание</span><span class="sxs-lookup"><span data-stu-id="30a74-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="30a74-121">contentBytes</span><span class="sxs-lookup"><span data-stu-id="30a74-121">contentBytes</span></span>|<span data-ttu-id="30a74-122">Двоичный</span><span class="sxs-lookup"><span data-stu-id="30a74-122">Binary</span></span>|<span data-ttu-id="30a74-123">Содержимое файла в кодировке base64.</span><span class="sxs-lookup"><span data-stu-id="30a74-123">The base64-encoded contents of the file.</span></span>|
|<span data-ttu-id="30a74-124">contentId</span><span class="sxs-lookup"><span data-stu-id="30a74-124">contentId</span></span>|<span data-ttu-id="30a74-125">String</span><span class="sxs-lookup"><span data-stu-id="30a74-125">String</span></span>|<span data-ttu-id="30a74-126">Идентификатор вложения в хранилище Exchange.</span><span class="sxs-lookup"><span data-stu-id="30a74-126">The ID of the attachment in the Exchange store.</span></span>|
|<span data-ttu-id="30a74-127">contentLocation</span><span class="sxs-lookup"><span data-stu-id="30a74-127">contentLocation</span></span>|<span data-ttu-id="30a74-128">String</span><span class="sxs-lookup"><span data-stu-id="30a74-128">String</span></span>|<span data-ttu-id="30a74-129">Универсальный код ресурса (URI), который соответствует расположению содержимого вложения.</span><span class="sxs-lookup"><span data-stu-id="30a74-129">The Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>|
|<span data-ttu-id="30a74-130">contentType</span><span class="sxs-lookup"><span data-stu-id="30a74-130">contentType</span></span>|<span data-ttu-id="30a74-131">String</span><span class="sxs-lookup"><span data-stu-id="30a74-131">String</span></span>|<span data-ttu-id="30a74-132">Тип контента этого вложения.</span><span class="sxs-lookup"><span data-stu-id="30a74-132">The content type of the attachment.</span></span>|
|<span data-ttu-id="30a74-133">id</span><span class="sxs-lookup"><span data-stu-id="30a74-133">id</span></span>|<span data-ttu-id="30a74-134">String</span><span class="sxs-lookup"><span data-stu-id="30a74-134">String</span></span>|<span data-ttu-id="30a74-135">Идентификатор вложения.</span><span class="sxs-lookup"><span data-stu-id="30a74-135">The attachment ID.</span></span>|
|<span data-ttu-id="30a74-136">isInline</span><span class="sxs-lookup"><span data-stu-id="30a74-136">isInline</span></span>|<span data-ttu-id="30a74-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="30a74-137">Boolean</span></span>|<span data-ttu-id="30a74-138">Задано значение true, если это встроенное вложение.</span><span class="sxs-lookup"><span data-stu-id="30a74-138">Set to true if this is an inline attachment.</span></span>|
|<span data-ttu-id="30a74-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="30a74-139">lastModifiedDateTime</span></span>|<span data-ttu-id="30a74-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="30a74-140">DateTimeOffset</span></span>|<span data-ttu-id="30a74-141">Дата и время последнего изменения вложения.</span><span class="sxs-lookup"><span data-stu-id="30a74-141">The date and time when the attachment was last modified.</span></span>|
|<span data-ttu-id="30a74-142">name</span><span class="sxs-lookup"><span data-stu-id="30a74-142">name</span></span>|<span data-ttu-id="30a74-143">String</span><span class="sxs-lookup"><span data-stu-id="30a74-143">String</span></span>|<span data-ttu-id="30a74-144">Имя, представляющее текст, который отображается под значком, представляющим внедренное вложение. Оно может не быть фактическим именем файла.</span><span class="sxs-lookup"><span data-stu-id="30a74-144">The name representing the text that is displayed below the icon representing the embedded attachment.This does not need to be the actual file name.</span></span>|
|<span data-ttu-id="30a74-145">size</span><span class="sxs-lookup"><span data-stu-id="30a74-145">size</span></span>|<span data-ttu-id="30a74-146">Int32</span><span class="sxs-lookup"><span data-stu-id="30a74-146">Int32</span></span>|<span data-ttu-id="30a74-147">Размер вложения в байтах.</span><span class="sxs-lookup"><span data-stu-id="30a74-147">The size in bytes of the attachment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="30a74-148">Связи</span><span class="sxs-lookup"><span data-stu-id="30a74-148">Relationships</span></span>
<span data-ttu-id="30a74-149">Нет</span><span class="sxs-lookup"><span data-stu-id="30a74-149">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="30a74-150">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="30a74-150">JSON representation</span></span>

<span data-ttu-id="30a74-151">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="30a74-151">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.attachment",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileAttachment"
}-->

```json
{
  "contentBytes": "binary",
  "contentId": "string",
  "contentLocation": "string",
  "contentType": "string",
  "id": "string (identifier)",
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "size": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fileAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
