---
title: Создание контакта
description: Добавление контакта в корневую папку с контактами или конечную точку `contacts` другой папки с контактами.
author: angelgolfer-ms
ms.openlocfilehash: 29432762aca0ad8d80b8d755ae3c0f45e754cb45
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321443"
---
# <a name="create-contact"></a><span data-ttu-id="88842-103">Создание контакта</span><span class="sxs-lookup"><span data-stu-id="88842-103">Create contact</span></span>

<span data-ttu-id="88842-104">Добавление контакта в корневую папку с контактами или конечную точку `contacts` другой папки с контактами.</span><span class="sxs-lookup"><span data-stu-id="88842-104">Add a contact to the root Contacts folder or to the `contacts` endpoint of another contact folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="88842-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="88842-105">Permissions</span></span>

<span data-ttu-id="88842-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="88842-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="88842-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="88842-108">Permission type</span></span>      | <span data-ttu-id="88842-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="88842-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="88842-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="88842-110">Delegated (work or school account)</span></span> | <span data-ttu-id="88842-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88842-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="88842-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="88842-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="88842-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88842-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="88842-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="88842-114">Application</span></span> | <span data-ttu-id="88842-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88842-115">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="88842-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="88842-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/contacts
POST /users/{id | userPrincipalName}/contacts

POST /me/contactFolders/{id}/contacts
POST /users/{id | userPrincipalName}/contactFolders/{id}/contacts
```

<br/>

## <a name="request-headers"></a><span data-ttu-id="88842-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="88842-117">Request headers</span></span>

| <span data-ttu-id="88842-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="88842-118">Header</span></span>       | <span data-ttu-id="88842-119">Значение</span><span class="sxs-lookup"><span data-stu-id="88842-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="88842-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="88842-120">Authorization</span></span>  | <span data-ttu-id="88842-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="88842-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="88842-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="88842-123">Content-Type</span></span>  | <span data-ttu-id="88842-p103">application/json. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="88842-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="88842-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="88842-126">Request body</span></span>
<span data-ttu-id="88842-127">В теле запроса представьте объект [Contact](../resources/contact.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="88842-127">In the request body, supply a JSON representation of the [Contact](../resources/contact.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="88842-128">Отклик</span><span class="sxs-lookup"><span data-stu-id="88842-128">Response</span></span>

<span data-ttu-id="88842-129">При успешном выполнении этот метод возвращает код отклика `201 Created` и объект [Contact](../resources/contact.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="88842-129">If successful, this method returns `201 Created` response code and the [Contact](../resources/contact.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="88842-130">Пример</span><span class="sxs-lookup"><span data-stu-id="88842-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="88842-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="88842-131">Request</span></span>

<span data-ttu-id="88842-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="88842-132">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_contact_from_contactfolder"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/contactFolders/{id}/contacts
Content-type: application/json
Content-length: 210

{
  "parentFolderId": "parentFolderId-value",
  "birthday": "datetime-value",
  "fileAs": "fileAs-value",
  "displayName": "displayName-value",
  "givenName": "givenName-value",
  "initials": "initials-value"
}
```

<br/>

<span data-ttu-id="88842-133">В теле запроса представьте объект [Contact](../resources/contact.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="88842-133">In the request body, supply a JSON representation of the [Contact](../resources/contact.md) object.</span></span>

### <a name="response"></a><span data-ttu-id="88842-134">Отклик</span><span class="sxs-lookup"><span data-stu-id="88842-134">Response</span></span>

<span data-ttu-id="88842-135">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="88842-135">Here is an example of the response.</span></span> <span data-ttu-id="88842-136">**Примечание.** Показанный здесь объект отклика может быть усечен для краткости.</span><span class="sxs-lookup"><span data-stu-id="88842-136">**Note:** The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="88842-137">При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="88842-137">All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 210

{
  "parentFolderId": "parentFolderId-value",
  "birthday": "datetime-value",
  "fileAs": "fileAs-value",
  "displayName": "displayName-value",
  "givenName": "givenName-value",
  "initials": "initials-value"
}
```

<br/>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
