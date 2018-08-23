# <a name="delete-mailfolder"></a><span data-ttu-id="520f8-101">Delete mailFolder</span><span class="sxs-lookup"><span data-stu-id="520f8-101">Delete mailFolder</span></span>

<span data-ttu-id="520f8-102">Удаление указанного объекта [mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="520f8-102">Delete the specified mailFolder object.</span></span>

<span data-ttu-id="520f8-103">Вы можете указать папку почты по ее идентификатору или по ее [имени известной папки](../resources/mailfolder.md), если оно существует.</span><span class="sxs-lookup"><span data-stu-id="520f8-103">You can specify a mail folder by its folder ID, or by its [well-known folder name](../resources/mailfolder.md), if one exists.</span></span> 

><span data-ttu-id="520f8-104">**Примечание** Возможно, вы не сможете удалить элементы в папке удаления восстанавливаемых элементов (представленной известным именем папки `recoverableitemsdeletions`).</span><span class="sxs-lookup"><span data-stu-id="520f8-104">**Note** You may not be able to delete items in the recoverable items deletions folder (represented by the well-known folder name `recoverableitemsdeletions`).</span></span> <span data-ttu-id="520f8-105">Подробнее см. статьи [Хранение удаленных элементов](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) и [Очистка удаленных элементов](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items).</span><span class="sxs-lookup"><span data-stu-id="520f8-105">See [Deleted item retention](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) and [Clean up deleted items](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) for more information.</span></span>

## <a name="permissions"></a><span data-ttu-id="520f8-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="520f8-106">Permissions</span></span>
<span data-ttu-id="520f8-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="520f8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="520f8-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="520f8-109">Permission type</span></span>      | <span data-ttu-id="520f8-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="520f8-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="520f8-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="520f8-111">Delegated (work or school account)</span></span> | <span data-ttu-id="520f8-112">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="520f8-112">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="520f8-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="520f8-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="520f8-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="520f8-114">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="520f8-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="520f8-115">Application</span></span> | <span data-ttu-id="520f8-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="520f8-116">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="520f8-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="520f8-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="520f8-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="520f8-118">Request headers</span></span>
| <span data-ttu-id="520f8-119">Имя</span><span class="sxs-lookup"><span data-stu-id="520f8-119">Name</span></span>       | <span data-ttu-id="520f8-120">Тип</span><span class="sxs-lookup"><span data-stu-id="520f8-120">Type</span></span> | <span data-ttu-id="520f8-121">Описание</span><span class="sxs-lookup"><span data-stu-id="520f8-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="520f8-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="520f8-122">Authorization</span></span>  | <span data-ttu-id="520f8-123">string</span><span class="sxs-lookup"><span data-stu-id="520f8-123">string</span></span>  | <span data-ttu-id="520f8-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="520f8-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="520f8-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="520f8-126">Request body</span></span>
<span data-ttu-id="520f8-127">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="520f8-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="520f8-128">Отклик</span><span class="sxs-lookup"><span data-stu-id="520f8-128">Response</span></span>

<span data-ttu-id="520f8-p104">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="520f8-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="520f8-131">Пример</span><span class="sxs-lookup"><span data-stu-id="520f8-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="520f8-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="520f8-132">Request</span></span>
<span data-ttu-id="520f8-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="520f8-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_mailfolder"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/mailFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="520f8-134">Ответ</span><span class="sxs-lookup"><span data-stu-id="520f8-134">Response</span></span>
<span data-ttu-id="520f8-135">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="520f8-135">Here is an example of the response.</span></span> 
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
  "description": "Delete mailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->