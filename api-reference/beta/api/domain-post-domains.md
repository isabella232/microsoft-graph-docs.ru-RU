---
title: Создание домена
description: Добавление домена в клиент.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 8f21ab37cf9648224e087ad193437eaabcb0a666
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984761"
---
# <a name="create-domain"></a><span data-ttu-id="837f4-103">Создание домена</span><span class="sxs-lookup"><span data-stu-id="837f4-103">Create domain</span></span>

> <span data-ttu-id="837f4-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="837f4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="837f4-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="837f4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="837f4-106">Добавление домена в клиент.</span><span class="sxs-lookup"><span data-stu-id="837f4-106">Adds a domain to the tenant.</span></span>

<span data-ttu-id="837f4-p102">**Важно!** Вам не удастся использовать сопоставленный домен с вашим клиентом Azure AD, пока не будет проверено владение доменом. Дополнительные сведения см. в статье [Перечисление verificationDnsRecords](domain-list-verificationdnsrecords.md). Для корневых доменов требуется проверка. Например, для домена contoso.com требуется проверка. Если корневой домен проверен, то его дочерние домены будут автоматически считаться проверенными. Например, если домен contoso.com проверен, то его дочерний домен subdomain.contoso.com будет автоматически считаться проверенным.</span><span class="sxs-lookup"><span data-stu-id="837f4-p102">**Important**: You cannot use an associated domain with your Azure AD tenant until ownership is verified. See [List verificationDnsRecords](domain-list-verificationdnsrecords.md) for details. Root domains require verification. For example, contoso.com requires verification. If a root domain is verified, subdomains of the root domain are automatically verified. For example, subdomain.contoso.com is automatically be verified if contoso.com has been verified.</span></span>

## <a name="permissions"></a><span data-ttu-id="837f4-113">Разрешения</span><span class="sxs-lookup"><span data-stu-id="837f4-113">Permissions</span></span>

<span data-ttu-id="837f4-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="837f4-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="837f4-116">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="837f4-116">Permission type</span></span>      | <span data-ttu-id="837f4-117">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="837f4-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="837f4-118">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="837f4-118">Delegated (work or school account)</span></span> | <span data-ttu-id="837f4-119">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="837f4-119">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="837f4-120">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="837f4-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="837f4-121">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="837f4-121">Not supported.</span></span>    |
|<span data-ttu-id="837f4-122">Для приложений</span><span class="sxs-lookup"><span data-stu-id="837f4-122">Application</span></span> | <span data-ttu-id="837f4-123">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="837f4-123">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="837f4-124">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="837f4-124">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /domains
```
## <a name="request-headers"></a><span data-ttu-id="837f4-125">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="837f4-125">Request headers</span></span>
| <span data-ttu-id="837f4-126">Имя</span><span class="sxs-lookup"><span data-stu-id="837f4-126">Name</span></span>       | <span data-ttu-id="837f4-127">Описание</span><span class="sxs-lookup"><span data-stu-id="837f4-127">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="837f4-128">Авторизация</span><span class="sxs-lookup"><span data-stu-id="837f4-128">Authorization</span></span>  | <span data-ttu-id="837f4-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="837f4-p104">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="837f4-131">Content-Type</span><span class="sxs-lookup"><span data-stu-id="837f4-131">Content-Type</span></span>  | <span data-ttu-id="837f4-132">application/json</span><span class="sxs-lookup"><span data-stu-id="837f4-132">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="837f4-133">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="837f4-133">Request body</span></span>
<span data-ttu-id="837f4-134">В теле запроса укажите представление JSON объекта [domain](../resources/domain.md).</span><span class="sxs-lookup"><span data-stu-id="837f4-134">In the request body, supply a JSON representation of [domain](../resources/domain.md) object.</span></span>

> <span data-ttu-id="837f4-p105">Тело запроса содержит свойство id для нового домена. id — это единственное свойство, которое можно указать, и оно является обязательным. Значение свойства id — полное доменное имя, которое необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="837f4-p105">The request body contains the id property for the new domain. Id is the only property that can be specified and it is required. The id property value is the fully qualified domain name to create.</span></span>

## <a name="response"></a><span data-ttu-id="837f4-138">Отклик</span><span class="sxs-lookup"><span data-stu-id="837f4-138">Response</span></span>

<span data-ttu-id="837f4-139">При успешном выполнении этот метод возвращает код отклика `201 Created` и объект [domain](../resources/domain.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="837f4-139">If successful, this method returns `201 Created` response code and [domain](../resources/domain.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="837f4-140">Пример</span><span class="sxs-lookup"><span data-stu-id="837f4-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="837f4-141">Запрос</span><span class="sxs-lookup"><span data-stu-id="837f4-141">Request</span></span>

<span data-ttu-id="837f4-142">В теле запроса укажите представление JSON объекта [domain](../resources/domain.md).</span><span class="sxs-lookup"><span data-stu-id="837f4-142">In the request body, supply a JSON representation of [domain](../resources/domain.md) object.</span></span>

<!-- {
  "blockType": "request",
  "id": "create_domain_from_domains"
}-->
```http
POST https://graph.microsoft.com/beta/domains
Content-type: application/json
Content-length: 192

{
  "id": "contoso.com"
}
```

##### <a name="response"></a><span data-ttu-id="837f4-143">Отклик</span><span class="sxs-lookup"><span data-stu-id="837f4-143">Response</span></span>
<span data-ttu-id="837f4-p106">Примечание. Представленный здесь объект отклика может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="837f4-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domain"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 192

{
  "authenticationType": "authenticationType-value",
  "availabilityStatus": "availabilityStatus-value",
  "id": "contoso.com",
  "isAdminManaged": true,
  "isDefault": true,
  "isInitial": true,
  "isRoot": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create domain",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
