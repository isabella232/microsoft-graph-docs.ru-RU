# <a name="chartfill-setsolidcolor"></a><span data-ttu-id="4ec3c-101">ChartFill: setSolidColor</span><span class="sxs-lookup"><span data-stu-id="4ec3c-101">ChartFill: setSolidColor</span></span>

<span data-ttu-id="4ec3c-102">Задает заливку одним цветом для элемента диаграммы.</span><span class="sxs-lookup"><span data-stu-id="4ec3c-102">Sets the fill formatting of a chart element to a uniform color.</span></span>
## <a name="permissions"></a><span data-ttu-id="4ec3c-103">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4ec3c-103">Permissions</span></span>
<span data-ttu-id="4ec3c-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4ec3c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4ec3c-106">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="4ec3c-106">Permission type</span></span>      | <span data-ttu-id="4ec3c-107">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="4ec3c-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4ec3c-108">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="4ec3c-108">Delegated (work or school account)</span></span> | <span data-ttu-id="4ec3c-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4ec3c-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4ec3c-110">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="4ec3c-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4ec3c-111">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4ec3c-111">Not supported.</span></span>    |
|<span data-ttu-id="4ec3c-112">Для приложений</span><span class="sxs-lookup"><span data-stu-id="4ec3c-112">Application</span></span> | <span data-ttu-id="4ec3c-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4ec3c-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4ec3c-114">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="4ec3c-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/format/fill/setSolidColor
POST /workbook/worksheets/{id|name}/charts(<name>)/title/format/fill/setSolidColor
POST /workbook/worksheets/{id|name}/charts(<name>)/legend/format/fill/setSolidColor

```
## <a name="request-headers"></a><span data-ttu-id="4ec3c-115">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="4ec3c-115">Request headers</span></span>
| <span data-ttu-id="4ec3c-116">Имя</span><span class="sxs-lookup"><span data-stu-id="4ec3c-116">Name</span></span>       | <span data-ttu-id="4ec3c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4ec3c-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4ec3c-118">Авторизация</span><span class="sxs-lookup"><span data-stu-id="4ec3c-118">Authorization</span></span>  | <span data-ttu-id="4ec3c-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4ec3c-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4ec3c-121">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="4ec3c-121">Request body</span></span>
<span data-ttu-id="4ec3c-122">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="4ec3c-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4ec3c-123">Параметр</span><span class="sxs-lookup"><span data-stu-id="4ec3c-123">Parameter</span></span>    | <span data-ttu-id="4ec3c-124">Тип</span><span class="sxs-lookup"><span data-stu-id="4ec3c-124">Type</span></span>   |<span data-ttu-id="4ec3c-125">Описание</span><span class="sxs-lookup"><span data-stu-id="4ec3c-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4ec3c-126">color</span><span class="sxs-lookup"><span data-stu-id="4ec3c-126">color</span></span>|<span data-ttu-id="4ec3c-127">string</span><span class="sxs-lookup"><span data-stu-id="4ec3c-127">string</span></span>|<span data-ttu-id="4ec3c-128">HTML-код, представляющий цвет линии границы в виде #RRGGBB (например, FFA500) или в виде ключевого слова (например, orange).</span><span class="sxs-lookup"><span data-stu-id="4ec3c-128">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|

## <a name="response"></a><span data-ttu-id="4ec3c-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="4ec3c-129">Response</span></span>

<span data-ttu-id="4ec3c-p103">В случае успешного выполнения этот метод возвращает код отклика `200 OK`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="4ec3c-p103">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4ec3c-132">Пример</span><span class="sxs-lookup"><span data-stu-id="4ec3c-132">Example</span></span>
<span data-ttu-id="4ec3c-133">Ниже приведен пример вызова этого API.</span><span class="sxs-lookup"><span data-stu-id="4ec3c-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="4ec3c-134">Запрос</span><span class="sxs-lookup"><span data-stu-id="4ec3c-134">Request</span></span>
<span data-ttu-id="4ec3c-135">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="4ec3c-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartfill_setsolidcolor"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/format/fill/setSolidColor
Content-type: application/json
Content-length: 28

{
  "color": "color-value"
}
```

##### <a name="response"></a><span data-ttu-id="4ec3c-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="4ec3c-136">Response</span></span>
<span data-ttu-id="4ec3c-137">Ниже приведен пример ответа.</span><span class="sxs-lookup"><span data-stu-id="4ec3c-137">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartFill: setSolidColor",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->