# <a name="delete-message"></a><span data-ttu-id="6ff4a-101">Удаление сообщения</span><span class="sxs-lookup"><span data-stu-id="6ff4a-101">Delete message</span></span>

<span data-ttu-id="6ff4a-102">Удаление сообщения.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-102">Delete message.</span></span>
## <a name="permissions"></a><span data-ttu-id="6ff4a-103">Разрешения</span><span class="sxs-lookup"><span data-stu-id="6ff4a-103">Permissions</span></span>
<span data-ttu-id="6ff4a-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6ff4a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6ff4a-106">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="6ff4a-106">Permission type</span></span>      | <span data-ttu-id="6ff4a-107">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="6ff4a-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="6ff4a-108">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6ff4a-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6ff4a-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6ff4a-109">Mail.ReadWrite</span></span>    | 
|<span data-ttu-id="6ff4a-110">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="6ff4a-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6ff4a-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6ff4a-111">Mail.ReadWrite</span></span>    | 
|<span data-ttu-id="6ff4a-112">Для приложений</span><span class="sxs-lookup"><span data-stu-id="6ff4a-112">Application</span></span> | <span data-ttu-id="6ff4a-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6ff4a-113">Mail.ReadWrite</span></span> | 

## <a name="http-request"></a><span data-ttu-id="6ff4a-114">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="6ff4a-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}
DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="6ff4a-115">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="6ff4a-115">Request headers</span></span>
| <span data-ttu-id="6ff4a-116">Имя</span><span class="sxs-lookup"><span data-stu-id="6ff4a-116">Name</span></span>       | <span data-ttu-id="6ff4a-117">Тип</span><span class="sxs-lookup"><span data-stu-id="6ff4a-117">Type</span></span> | <span data-ttu-id="6ff4a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6ff4a-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6ff4a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="6ff4a-119">Authorization</span></span>  | <span data-ttu-id="6ff4a-120">string</span><span class="sxs-lookup"><span data-stu-id="6ff4a-120">string</span></span>  | <span data-ttu-id="6ff4a-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6ff4a-123">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="6ff4a-123">Request body</span></span>
<span data-ttu-id="6ff4a-124">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6ff4a-125">Отклик</span><span class="sxs-lookup"><span data-stu-id="6ff4a-125">Response</span></span>

<span data-ttu-id="6ff4a-p103">В случае успешного выполнения этот метод возвращает код отклика `204, No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6ff4a-128">Пример</span><span class="sxs-lookup"><span data-stu-id="6ff4a-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6ff4a-129">Запрос</span><span class="sxs-lookup"><span data-stu-id="6ff4a-129">Request</span></span>
<span data-ttu-id="6ff4a-130">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_message"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="6ff4a-131">Отклик</span><span class="sxs-lookup"><span data-stu-id="6ff4a-131">Response</span></span>
<span data-ttu-id="6ff4a-132">Ниже приведен пример ответа.</span><span class="sxs-lookup"><span data-stu-id="6ff4a-132">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->