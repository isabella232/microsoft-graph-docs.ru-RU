# <a name="delete-domain"></a><span data-ttu-id="eb541-101">Удаление домена</span><span class="sxs-lookup"><span data-stu-id="eb541-101">Delete domain</span></span>

<span data-ttu-id="eb541-102">Удаление домена из клиента.</span><span class="sxs-lookup"><span data-stu-id="eb541-102">Deletes a domain from a tenant.</span></span>

> <span data-ttu-id="eb541-103">**Важно!**</span><span class="sxs-lookup"><span data-stu-id="eb541-103">**Important:**</span></span>
> - <span data-ttu-id="eb541-104">Вам не удастся восстановить удаленные домены.</span><span class="sxs-lookup"><span data-stu-id="eb541-104">Deleted domains are not recoverable.</span></span><br />
> - <span data-ttu-id="eb541-p101">Вам не удастся удалить домен, если какие-либо ресурсы или объекты все еще зависят от него. Вы можете найти все зависимые ресурсы с помощью API [перечисления domainNameReferences](domain_list_domainnamereferences.md).</span><span class="sxs-lookup"><span data-stu-id="eb541-p101">Attempts to delete will fail if there are any resources or objects still dependent on the domain. You can find all dependent resources by using the [List domainNameReferences](domain_list_domainnamereferences.md) API.</span></span>

## <a name="permissions"></a><span data-ttu-id="eb541-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="eb541-107">Permissions</span></span>

<span data-ttu-id="eb541-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="eb541-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="eb541-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="eb541-110">Permission type</span></span>      | <span data-ttu-id="eb541-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="eb541-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eb541-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="eb541-112">Delegated (work or school account)</span></span> | <span data-ttu-id="eb541-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="eb541-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="eb541-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="eb541-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eb541-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eb541-115">Not supported.</span></span>    |
|<span data-ttu-id="eb541-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="eb541-116">Application</span></span> | <span data-ttu-id="eb541-117">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb541-117">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="eb541-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="eb541-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /domains/{id}
```

> <span data-ttu-id="eb541-119">В качестве параметра {id} укажите домен, используя его полное доменное имя.</span><span class="sxs-lookup"><span data-stu-id="eb541-119">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="eb541-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="eb541-120">Request headers</span></span>

| <span data-ttu-id="eb541-121">Имя</span><span class="sxs-lookup"><span data-stu-id="eb541-121">Name</span></span>       | <span data-ttu-id="eb541-122">Описание</span><span class="sxs-lookup"><span data-stu-id="eb541-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="eb541-123">Авторизация</span><span class="sxs-lookup"><span data-stu-id="eb541-123">Authorization</span></span>  | <span data-ttu-id="eb541-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eb541-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="eb541-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="eb541-126">Content-Type</span></span>  | <span data-ttu-id="eb541-127">application/json</span><span class="sxs-lookup"><span data-stu-id="eb541-127">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="eb541-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="eb541-128">Request body</span></span>

<span data-ttu-id="eb541-129">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="eb541-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eb541-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="eb541-130">Response</span></span>

<span data-ttu-id="eb541-p104">При успешном выполнении этот метод возвращает код отклика `204, No Content`. Он не возвращает тело отклика.</span><span class="sxs-lookup"><span data-stu-id="eb541-p104">If successful, this method returns `204, No Content` response code. It does not return a response body.</span></span>

## <a name="example"></a><span data-ttu-id="eb541-133">Пример</span><span class="sxs-lookup"><span data-stu-id="eb541-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eb541-134">Запрос</span><span class="sxs-lookup"><span data-stu-id="eb541-134">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_domain"
}-->
```http
DELETE https://graph.microsoft.com/V1.0/domains/contoso.com
```

##### <a name="response"></a><span data-ttu-id="eb541-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="eb541-135">Response</span></span>

<span data-ttu-id="eb541-p105">Примечание. Представленный здесь объект отклика может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="eb541-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete domain",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->