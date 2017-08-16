# <a name="list-manager"></a><span data-ttu-id="20266-101">Получение руководителя</span><span class="sxs-lookup"><span data-stu-id="20266-101">List manager</span></span>

<span data-ttu-id="20266-p101">Получение руководителя пользователя. Возвращает пользователя или контакт, назначенный руководителем пользователя.</span><span class="sxs-lookup"><span data-stu-id="20266-p101">Get user's manager. Returns the user or contact assigned as the user's manager.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="20266-104">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="20266-104">Prerequisites</span></span>
<span data-ttu-id="20266-105">Для применения этого API требуется одна из указанных **областей**: *User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="20266-105">One of the following **scopes** is required to execute this API: *User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="20266-106">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="20266-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/manager
```
## <a name="optional-query-parameters"></a><span data-ttu-id="20266-107">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="20266-107">Optional query parameters</span></span>
<span data-ttu-id="20266-108">Этот метод поддерживает [параметры запросов OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="20266-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="20266-109">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="20266-109">Request headers</span></span>
| <span data-ttu-id="20266-110">Заголовок</span><span class="sxs-lookup"><span data-stu-id="20266-110">Header</span></span>       | <span data-ttu-id="20266-111">Значение</span><span class="sxs-lookup"><span data-stu-id="20266-111">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="20266-112">Авторизация</span><span class="sxs-lookup"><span data-stu-id="20266-112">Authorization</span></span>  | <span data-ttu-id="20266-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="20266-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="20266-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="20266-115">Content-Type</span></span>   | <span data-ttu-id="20266-116">application/json</span><span class="sxs-lookup"><span data-stu-id="20266-116">application/json</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="20266-117">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="20266-117">Request body</span></span>
<span data-ttu-id="20266-118">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="20266-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="20266-119">Отклик</span><span class="sxs-lookup"><span data-stu-id="20266-119">Response</span></span>

<span data-ttu-id="20266-120">В случае успеха этот метод возвращает код отклика `200 OK` и объект [directoryObject](../resources/directoryobject.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="20266-120">If successful, this method returns a `200 OK` response code and a [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="20266-121">Пример</span><span class="sxs-lookup"><span data-stu-id="20266-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="20266-122">Запрос</span><span class="sxs-lookup"><span data-stu-id="20266-122">Request</span></span>
<span data-ttu-id="20266-123">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="20266-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_manager"
}-->
```http
GET https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/manager
```
##### <a name="response"></a><span data-ttu-id="20266-124">Отклик</span><span class="sxs-lookup"><span data-stu-id="20266-124">Response</span></span>
<span data-ttu-id="20266-125">Ниже приведен пример ответа.</span><span class="sxs-lookup"><span data-stu-id="20266-125">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "objectType": "User",
  "id": "111048d2-2761-4347-b978-07354283363b",
  "accountEnabled": true,
  "city": "San Diego",
  "country": "United States",
  "department": "Sales & Marketing",
  "displayName": "Sara Davis",
  "givenName": "Sara",
  "jobTitle": "Finance VP",
  "mail": "SaraD@contoso.onmicrosoft.com",
  "mailNickname": "SaraD",
  "state": "CA",
  "streetAddress": "9256 Towne Center Dr., Suite 400",
  "surname": "Davis",
  "usageLocation": "US",
  "userPrincipalName": "SaraD@contoso.onmicrosoft.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directReports",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
