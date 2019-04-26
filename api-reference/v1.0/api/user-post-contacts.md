---
title: Создание объекта Contact
description: Добавление контакта в корневую папку с контактами или конечную точку контактов другой папки с контактами.
author: dkershaw10
localization_priority: Priority
ms.prod: microsoft-identity-platform
ms.openlocfilehash: bd2bdfdbfc5242a49085c236171b86cd7aa29f3a
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32564073"
---
# <a name="create-contact"></a><span data-ttu-id="90844-103">Создание объекта Contact</span><span class="sxs-lookup"><span data-stu-id="90844-103">Create Contact</span></span>

<span data-ttu-id="90844-104">Добавление контакта в корневую папку с контактами или конечную точку contacts другой папки с контактами.</span><span class="sxs-lookup"><span data-stu-id="90844-104">Add a contact to the root Contacts folder or to the contacts endpoint of another contact folder.</span></span>
## <a name="permissions"></a><span data-ttu-id="90844-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="90844-105">Permissions</span></span>
<span data-ttu-id="90844-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="90844-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="90844-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="90844-108">Permission type</span></span>      | <span data-ttu-id="90844-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="90844-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="90844-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="90844-110">Delegated (work or school account)</span></span> | <span data-ttu-id="90844-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="90844-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="90844-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="90844-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="90844-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="90844-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="90844-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="90844-114">Application</span></span> | <span data-ttu-id="90844-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="90844-115">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="90844-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="90844-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contacts
POST /users/{id | userPrincipalName}/contacts
POST /me/contactFolders/{contactFolderId}/contacts
POST /users/{id | userPrincipalName}/contactFolders/{contactFolderId}/contacts
```
## <a name="request-headers"></a><span data-ttu-id="90844-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="90844-117">Request headers</span></span>
| <span data-ttu-id="90844-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="90844-118">Header</span></span>       | <span data-ttu-id="90844-119">Значение</span><span class="sxs-lookup"><span data-stu-id="90844-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="90844-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="90844-120">Authorization</span></span>  | <span data-ttu-id="90844-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="90844-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="90844-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="90844-123">Content-Type</span></span>  | <span data-ttu-id="90844-124">application/json</span><span class="sxs-lookup"><span data-stu-id="90844-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="90844-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="90844-125">Request body</span></span>
<span data-ttu-id="90844-126">Предоставьте в тексте запроса описание объекта [Contact](../resources/contact.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="90844-126">In the request body, supply a JSON representation of [Contact](../resources/contact.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="90844-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="90844-127">Response</span></span>

<span data-ttu-id="90844-128">В случае успеха этот метод возвращает код отклика `201 Created` и объект [Contact](../resources/contact.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="90844-128">If successful, this method returns `201 Created` response code and [Contact](../resources/contact.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="90844-129">Пример</span><span class="sxs-lookup"><span data-stu-id="90844-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="90844-130">Запрос</span><span class="sxs-lookup"><span data-stu-id="90844-130">Request</span></span>
<span data-ttu-id="90844-131">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="90844-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contact_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/contacts
Content-type: application/json

{
  "givenName": "Pavel",
  "surname": "Bansky",
  "emailAddresses": [
    {
      "address": "pavelb@fabrikam.onmicrosoft.com",
      "name": "Pavel Bansky"
    }
  ],
  "businessPhones": [
    "+1 732 555 0102"
  ]
}
```
<span data-ttu-id="90844-132">Предоставьте в тексте запроса описание объекта [contact](../resources/contact.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="90844-132">In the request body, supply a JSON representation of [contact](../resources/contact.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="90844-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="90844-133">Response</span></span>
<span data-ttu-id="90844-p103">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="90844-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "id-value",
  "createdDateTime": "2015-11-09T02:14:32Z",
  "lastModifiedDateTime": "2015-11-09T02:14:32Z",
   "displayName": "Pavel Bansky"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
