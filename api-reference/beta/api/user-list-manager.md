---
title: Получение руководителя
description: Получение руководителя пользователя. Возвращает пользователя или контакт, назначенный в качестве руководителя пользователя.
localization_priority: Normal
author: krbain
ms.prod: users
doc_type: apiPageType
ms.openlocfilehash: 363befccc797da2d93cf1ddf4eb68f5303de51c2
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "48400846"
---
# <a name="list-manager"></a><span data-ttu-id="a76a6-104">Получение руководителя</span><span class="sxs-lookup"><span data-stu-id="a76a6-104">List manager</span></span>

<span data-ttu-id="a76a6-105">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="a76a6-105">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="a76a6-106">Получение руководителя пользователя.</span><span class="sxs-lookup"><span data-stu-id="a76a6-106">Get user's manager.</span></span> <span data-ttu-id="a76a6-107">Возвращает пользователя или контакт, назначенный в качестве руководителя пользователя.</span><span class="sxs-lookup"><span data-stu-id="a76a6-107">Returns the user or contact assigned as the user's manager.</span></span>
## <a name="permissions"></a><span data-ttu-id="a76a6-108">Разрешения</span><span class="sxs-lookup"><span data-stu-id="a76a6-108">Permissions</span></span>
<span data-ttu-id="a76a6-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a76a6-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a76a6-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="a76a6-111">Permission type</span></span>      | <span data-ttu-id="a76a6-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="a76a6-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a76a6-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a76a6-113">Delegated (work or school account)</span></span> | <span data-ttu-id="a76a6-114">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a76a6-114">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="a76a6-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="a76a6-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a76a6-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a76a6-116">Not supported.</span></span>    |
|<span data-ttu-id="a76a6-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="a76a6-117">Application</span></span> | <span data-ttu-id="a76a6-118">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a76a6-118">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

[!INCLUDE [limited-info](../../includes/limited-info.md)]

## <a name="http-request"></a><span data-ttu-id="a76a6-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="a76a6-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/manager
GET /users/{id | userPrincipalName}/manager
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a76a6-120">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="a76a6-120">Optional query parameters</span></span>
<span data-ttu-id="a76a6-121">Этот метод поддерживает [параметры запросов OData](/graph/query-parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="a76a6-121">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a76a6-122">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="a76a6-122">Request headers</span></span>
| <span data-ttu-id="a76a6-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a76a6-123">Header</span></span>       | <span data-ttu-id="a76a6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a76a6-124">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="a76a6-125">Авторизация</span><span class="sxs-lookup"><span data-stu-id="a76a6-125">Authorization</span></span>  | <span data-ttu-id="a76a6-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a76a6-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a76a6-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a76a6-128">Content-Type</span></span>   | <span data-ttu-id="a76a6-129">application/json</span><span class="sxs-lookup"><span data-stu-id="a76a6-129">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a76a6-130">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="a76a6-130">Request body</span></span>
<span data-ttu-id="a76a6-131">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="a76a6-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a76a6-132">Отклик</span><span class="sxs-lookup"><span data-stu-id="a76a6-132">Response</span></span>

<span data-ttu-id="a76a6-133">В случае успеха этот метод возвращает код отклика `200 OK` и объект [directoryObject](../resources/directoryobject.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="a76a6-133">If successful, this method returns a `200 OK` response code and a [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a76a6-134">Пример</span><span class="sxs-lookup"><span data-stu-id="a76a6-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a76a6-135">Запрос</span><span class="sxs-lookup"><span data-stu-id="a76a6-135">Request</span></span>
<span data-ttu-id="a76a6-136">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="a76a6-136">Here is an example of the request.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/users/{id|userPrincipalName}/manager
```
##### <a name="response"></a><span data-ttu-id="a76a6-137">Отклик</span><span class="sxs-lookup"><span data-stu-id="a76a6-137">Response</span></span>
<span data-ttu-id="a76a6-138">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="a76a6-138">Here is an example of the response.</span></span>
<!-- { "blockType": "ignored" } -->
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
<!--
{
  "type": "#page.annotation",
  "description": "List directReports",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->