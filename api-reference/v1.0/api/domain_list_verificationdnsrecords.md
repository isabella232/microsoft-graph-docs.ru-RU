# <a name="list-verificationdnsrecords"></a><span data-ttu-id="0b80c-101">Перечисление verificationDnsRecords</span><span class="sxs-lookup"><span data-stu-id="0b80c-101">List verificationDnsRecords</span></span>

<span data-ttu-id="0b80c-102">Получение списка объектов [domainDnsRecord](../resources/domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="0b80c-102">Retrieve a list of [domainDnsRecord](../resources/domaindnsrecord.md) objects.</span></span>

<span data-ttu-id="0b80c-p101">Вам не удастся использовать сопоставленный домен с вашим клиентом Azure AD, пока не будет проверено владение доменом. Чтобы подтвердить владение доменом, получите записи проверки домена и добавьте сведения в файл зоны домена. Это можно сделать с помощью регистратора доменных имен или путем настройки DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="0b80c-p101">You cannot use an associated domain with your Azure AD tenant until ownership is verified. To verify the ownership of the domain, retrieve the domain verification records and add the details to the zone file of the domain. This can be done through the domain registrar or DNS server configuration.</span></span>

<span data-ttu-id="0b80c-p102">Для корневых доменов требуется проверка. Например, для домена contoso.com требуется проверка. Если корневой домен проверен, то его дочерние домены будут автоматически считаться проверенными. Например, если домен contoso.com проверен, то его дочерний домен subdomain.contoso.com будет автоматически считаться проверенным.</span><span class="sxs-lookup"><span data-stu-id="0b80c-p102">Root domains require verification. For example, contoso.com requires verification. If a root domain is verified, subdomains of the root domain are automatically verified. For example, subdomain.contoso.com is automatically be verified if contoso.com has been verified.</span></span>

## <a name="permissions"></a><span data-ttu-id="0b80c-110">Разрешения</span><span class="sxs-lookup"><span data-stu-id="0b80c-110">Permissions</span></span>

<span data-ttu-id="0b80c-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0b80c-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="0b80c-113">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="0b80c-113">Permission type</span></span>      | <span data-ttu-id="0b80c-114">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="0b80c-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0b80c-115">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="0b80c-115">Delegated (work or school account)</span></span> | <span data-ttu-id="0b80c-116">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="0b80c-116">Directory.Read.All</span></span>    |
|<span data-ttu-id="0b80c-117">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="0b80c-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0b80c-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0b80c-118">Not supported.</span></span>    |
|<span data-ttu-id="0b80c-119">Для приложений</span><span class="sxs-lookup"><span data-stu-id="0b80c-119">Application</span></span> | <span data-ttu-id="0b80c-120">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b80c-120">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0b80c-121">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="0b80c-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}/verificationDnsRecords
```

> <span data-ttu-id="0b80c-122">В качестве параметра {id} укажите домен, используя его полное доменное имя.</span><span class="sxs-lookup"><span data-stu-id="0b80c-122">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="0b80c-123">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="0b80c-123">Optional query parameters</span></span>

<span data-ttu-id="0b80c-124">Этот метод поддерживает [параметры запросов OData](http://graph.microsoft.io/docs/overview/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="0b80c-124">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0b80c-125">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="0b80c-125">Request headers</span></span>

| <span data-ttu-id="0b80c-126">Имя</span><span class="sxs-lookup"><span data-stu-id="0b80c-126">Name</span></span>      |<span data-ttu-id="0b80c-127">Описание</span><span class="sxs-lookup"><span data-stu-id="0b80c-127">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="0b80c-128">Авторизация</span><span class="sxs-lookup"><span data-stu-id="0b80c-128">Authorization</span></span>  | <span data-ttu-id="0b80c-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="0b80c-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0b80c-131">Content-Type</span><span class="sxs-lookup"><span data-stu-id="0b80c-131">Content-Type</span></span>  | <span data-ttu-id="0b80c-132">application/json</span><span class="sxs-lookup"><span data-stu-id="0b80c-132">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="0b80c-133">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="0b80c-133">Request body</span></span>

<span data-ttu-id="0b80c-134">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="0b80c-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0b80c-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="0b80c-135">Response</span></span>

<span data-ttu-id="0b80c-136">При успешном выполнении этот метод возвращает код отклика `200 OK` и коллекцию объектов [domainDnsRecord](../resources/domaindnsrecord.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="0b80c-136">If successful, this method returns a `200 OK` response code and collection of [domainDnsRecord](../resources/domaindnsrecord.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0b80c-137">Пример</span><span class="sxs-lookup"><span data-stu-id="0b80c-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0b80c-138">Запрос</span><span class="sxs-lookup"><span data-stu-id="0b80c-138">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_verificationdnsrecords"
}-->
```http
GET https://graph.microsoft.com/v1.0/domains/{domain-name}/verificationDnsRecords
```

##### <a name="response"></a><span data-ttu-id="0b80c-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="0b80c-139">Response</span></span>

<span data-ttu-id="0b80c-p105">Примечание. Представленный здесь объект отклика может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="0b80c-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domainDnsRecord",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 220

{
  "value": [
    {
      "isOptional": false,
      "label": "contoso.com",
      "recordType": "Mx",
      "supportedService": "Email",
      "ttl": 3600,
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List verificationDnsRecords",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->