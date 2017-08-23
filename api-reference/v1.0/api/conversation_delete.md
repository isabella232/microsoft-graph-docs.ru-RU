# <a name="delete-conversation"></a><span data-ttu-id="1c990-101">Удаление беседы</span><span class="sxs-lookup"><span data-stu-id="1c990-101">Delete conversation</span></span>

<span data-ttu-id="1c990-102">Удаление беседы.</span><span class="sxs-lookup"><span data-stu-id="1c990-102">Delete conversation.</span></span>
## <a name="permissions"></a><span data-ttu-id="1c990-103">Разрешения</span><span class="sxs-lookup"><span data-stu-id="1c990-103">Permissions</span></span>
<span data-ttu-id="1c990-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1c990-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1c990-106">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="1c990-106">Permission type</span></span>      | <span data-ttu-id="1c990-107">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="1c990-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="1c990-108">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="1c990-108">Delegated (work or school account)</span></span> | <span data-ttu-id="1c990-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1c990-109">Group.ReadWrite.All</span></span>    | 
|<span data-ttu-id="1c990-110">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="1c990-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1c990-111">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1c990-111">Not supported.</span></span>    | 
|<span data-ttu-id="1c990-112">Для приложений</span><span class="sxs-lookup"><span data-stu-id="1c990-112">Application</span></span> | <span data-ttu-id="1c990-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1c990-113">Group.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="1c990-114">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="1c990-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/conversations/{id}
```
## <a name="request-headers"></a><span data-ttu-id="1c990-115">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="1c990-115">Request headers</span></span>
| <span data-ttu-id="1c990-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1c990-116">Header</span></span>       | <span data-ttu-id="1c990-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1c990-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1c990-118">Авторизация</span><span class="sxs-lookup"><span data-stu-id="1c990-118">Authorization</span></span>  | <span data-ttu-id="1c990-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="1c990-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1c990-121">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="1c990-121">Request body</span></span>
<span data-ttu-id="1c990-122">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="1c990-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1c990-123">Отклик</span><span class="sxs-lookup"><span data-stu-id="1c990-123">Response</span></span>

<span data-ttu-id="1c990-p103">В случае успешного выполнения этот метод возвращает код отклика `204, No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="1c990-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1c990-126">Пример</span><span class="sxs-lookup"><span data-stu-id="1c990-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1c990-127">Запрос</span><span class="sxs-lookup"><span data-stu-id="1c990-127">Request</span></span>
<span data-ttu-id="1c990-128">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="1c990-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_conversation"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/conversations/{id}
```
##### <a name="response"></a><span data-ttu-id="1c990-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="1c990-129">Response</span></span>
<span data-ttu-id="1c990-130">Ниже приведен пример ответа.</span><span class="sxs-lookup"><span data-stu-id="1c990-130">Here is an example of the response.</span></span> 
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
  "description": "Delete conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
