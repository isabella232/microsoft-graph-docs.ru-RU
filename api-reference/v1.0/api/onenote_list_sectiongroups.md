# <a name="list-sectiongroups"></a><span data-ttu-id="6e416-101">Перечисление sectionGroups</span><span class="sxs-lookup"><span data-stu-id="6e416-101">List sectionGroups</span></span>

<span data-ttu-id="6e416-102">Получение списка объектов [sectionGroup](../resources/sectiongroup.md).</span><span class="sxs-lookup"><span data-stu-id="6e416-102">Retrieve a list of [sectionGroup](../resources/sectiongroup.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="6e416-103">Разрешения</span><span class="sxs-lookup"><span data-stu-id="6e416-103">Permissions</span></span>
<span data-ttu-id="6e416-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6e416-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6e416-106">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="6e416-106">Permission type</span></span>      | <span data-ttu-id="6e416-107">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="6e416-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="6e416-108">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6e416-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6e416-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6e416-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    | 
|<span data-ttu-id="6e416-110">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="6e416-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6e416-111">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e416-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    | 
|<span data-ttu-id="6e416-112">Для приложений</span><span class="sxs-lookup"><span data-stu-id="6e416-112">Application</span></span> | <span data-ttu-id="6e416-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6e416-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="6e416-114">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="6e416-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups
GET /users/{id | userPrincipalName}/onenote/sectionGroups
GET /groups/{id}/onenote/sectionGroups
GET /sites/{id}/onenote/sectionGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6e416-115">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="6e416-115">Optional query parameters</span></span>
<span data-ttu-id="6e416-116">Этот метод поддерживает [параметры запросов OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) для настройки отклика.</span><span class="sxs-lookup"><span data-stu-id="6e416-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="6e416-117">По умолчанию используется порядок сортировки `name asc`.</span><span class="sxs-lookup"><span data-stu-id="6e416-117">The default sort order is `name asc`.</span></span>

<span data-ttu-id="6e416-p102">Запрос, используемый по умолчанию, разворачивает `parentNotebook` и выбирает соответствующие свойства `id`, `displayName` и `self`. Допустимые значения `expand` для групп разделов: `sections`, `sectionGroups`, `parentNotebook` и `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="6e416-p102">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for section groups are `sections`, `sectionGroups`, `parentNotebook`, and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6e416-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="6e416-120">Request headers</span></span>
| <span data-ttu-id="6e416-121">Имя</span><span class="sxs-lookup"><span data-stu-id="6e416-121">Name</span></span>       | <span data-ttu-id="6e416-122">Тип</span><span class="sxs-lookup"><span data-stu-id="6e416-122">Type</span></span> | <span data-ttu-id="6e416-123">Описание</span><span class="sxs-lookup"><span data-stu-id="6e416-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6e416-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="6e416-124">Authorization</span></span>  | <span data-ttu-id="6e416-125">string</span><span class="sxs-lookup"><span data-stu-id="6e416-125">string</span></span>  | <span data-ttu-id="6e416-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6e416-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6e416-128">Accept</span><span class="sxs-lookup"><span data-stu-id="6e416-128">Accept</span></span> | <span data-ttu-id="6e416-129">строка</span><span class="sxs-lookup"><span data-stu-id="6e416-129">string</span></span> | `application/json` |  

## <a name="request-body"></a><span data-ttu-id="6e416-130">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="6e416-130">Request body</span></span>
<span data-ttu-id="6e416-131">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="6e416-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6e416-132">Отклик</span><span class="sxs-lookup"><span data-stu-id="6e416-132">Response</span></span>

<span data-ttu-id="6e416-133">При успешном выполнении этот метод возвращает код отклика `200 OK` и коллекцию объектов [sectionGroup](../resources/sectiongroup.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="6e416-133">If successful, this method returns a `200 OK` response code and collection of [sectionGroup](../resources/sectiongroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6e416-134">Пример</span><span class="sxs-lookup"><span data-stu-id="6e416-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6e416-135">Запрос</span><span class="sxs-lookup"><span data-stu-id="6e416-135">Request</span></span>
<span data-ttu-id="6e416-136">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="6e416-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sectiongroups"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sectionGroups
```
##### <a name="response"></a><span data-ttu-id="6e416-137">Отклик</span><span class="sxs-lookup"><span data-stu-id="6e416-137">Response</span></span>
<span data-ttu-id="6e416-p104">Ниже приведен пример отклика. Примечание. Показанный здесь объект ответа усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="6e416-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sectiongroup",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 378

{
  "value": [
    {
      "sectionsUrl": "sectionsUrl-value",
      "sectionGroupsUrl": "sectionGroupsUrl-value",
      "displayName": "name-value",      
      "createdBy": {
        "user": {
          "id": "id-value",
          "displayName": "displayName-value"
        }
      },
      "lastModifiedBy": {
        "user": {
          "id": "id-value",
          "displayName": "displayName-value"
        }
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List sectionGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->