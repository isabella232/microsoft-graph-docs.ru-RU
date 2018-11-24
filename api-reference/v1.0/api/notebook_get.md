# <a name="get-notebook"></a><span data-ttu-id="80400-101">Получение записной книжки</span><span class="sxs-lookup"><span data-stu-id="80400-101">Get notebook</span></span>

<span data-ttu-id="80400-102">Получение свойств и связей объекта [notebook](../resources/notebook.md).</span><span class="sxs-lookup"><span data-stu-id="80400-102">Retrieve the properties and relationships of a [notebook](../resources/notebook.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="80400-103">Разрешения</span><span class="sxs-lookup"><span data-stu-id="80400-103">Permissions</span></span>
<span data-ttu-id="80400-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="80400-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="80400-106">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="80400-106">Permission type</span></span>      | <span data-ttu-id="80400-107">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="80400-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="80400-108">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="80400-108">Delegated (work or school account)</span></span> | <span data-ttu-id="80400-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="80400-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="80400-110">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="80400-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="80400-111">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="80400-111">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="80400-112">Для приложений</span><span class="sxs-lookup"><span data-stu-id="80400-112">Application</span></span> | <span data-ttu-id="80400-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="80400-113">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="80400-114">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="80400-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/{id}
GET /users/{id | userPrincipalName}/onenote/notebooks/{id}
GET /groups/{id}/onenote/notebooks/{id}
GET /sites/{id}/onenote/notebooks/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="80400-115">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="80400-115">Optional query parameters</span></span>
<span data-ttu-id="80400-116">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) `select` и `expand` для настройки отклика.</span><span class="sxs-lookup"><span data-stu-id="80400-116">This method supports the `select` and `expand` [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="80400-117">Допустимые значения `expand` для записных книжек: `sections` и `sectionGroups`.</span><span class="sxs-lookup"><span data-stu-id="80400-117">Valid `expand` values for notebooks are `sections` and `sectionGroups`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="80400-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="80400-118">Request headers</span></span>
| <span data-ttu-id="80400-119">Имя</span><span class="sxs-lookup"><span data-stu-id="80400-119">Name</span></span>       | <span data-ttu-id="80400-120">Тип</span><span class="sxs-lookup"><span data-stu-id="80400-120">Type</span></span> | <span data-ttu-id="80400-121">Описание</span><span class="sxs-lookup"><span data-stu-id="80400-121">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="80400-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="80400-122">Authorization</span></span>  | <span data-ttu-id="80400-123">string</span><span class="sxs-lookup"><span data-stu-id="80400-123">string</span></span>  | <span data-ttu-id="80400-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="80400-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="80400-126">Accept</span><span class="sxs-lookup"><span data-stu-id="80400-126">Accept</span></span> | <span data-ttu-id="80400-127">строка</span><span class="sxs-lookup"><span data-stu-id="80400-127">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="80400-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="80400-128">Request body</span></span>
<span data-ttu-id="80400-129">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="80400-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="80400-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="80400-130">Response</span></span>

<span data-ttu-id="80400-131">При успешном выполнении этот метод возвращает код отклика `200 OK` и объект [notebook](../resources/notebook.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="80400-131">If successful, this method returns a `200 OK` response code and a [notebook](../resources/notebook.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="80400-132">Пример</span><span class="sxs-lookup"><span data-stu-id="80400-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="80400-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="80400-133">Request</span></span>
<span data-ttu-id="80400-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="80400-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_notebook"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}
```
##### <a name="response"></a><span data-ttu-id="80400-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="80400-135">Response</span></span>
<span data-ttu-id="80400-p103">Ниже приведен пример отклика. Примечание. Показанный здесь объект ответа усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="80400-p103">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 284

{
  "isDefault": true,
  "userRole": {
  },
  "isShared": true,
  "sectionsUrl": "sectionsUrl-value",
  "sectionGroupsUrl": "sectionGroupsUrl-value",
  "links": {
    "oneNoteClientUrl": {
      "href": "href-value"
    },
    "oneNoteWebUrl": {
      "href": "href-value"
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get notebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
