---
title: Удаление servicePrincipal
description: Удаление servicePrincipal.
localization_priority: Normal
doc_type: apiPageType
ms.prod: microsoft-identity-platform
author: davidmu1
ms.openlocfilehash: 2731a23dea3de57d588ceec304a1155a6c09a34d
ms.sourcegitcommit: 87966dcd42a0111c5c9987fcae0a491c92022938
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "44291288"
---
# <a name="delete-serviceprincipal"></a><span data-ttu-id="aa378-103">Удаление servicePrincipal</span><span class="sxs-lookup"><span data-stu-id="aa378-103">Delete servicePrincipal</span></span>

<span data-ttu-id="aa378-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="aa378-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="aa378-105">Удаление объекта [servicePrincipal](../resources/serviceprincipal.md) .</span><span class="sxs-lookup"><span data-stu-id="aa378-105">Delete a [servicePrincipal](../resources/serviceprincipal.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="aa378-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="aa378-106">Permissions</span></span>
<span data-ttu-id="aa378-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aa378-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aa378-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="aa378-109">Permission type</span></span>      | <span data-ttu-id="aa378-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="aa378-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="aa378-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="aa378-111">Delegated (work or school account)</span></span> | <span data-ttu-id="aa378-112">Application. ReadWrite. ALL, Directory. ReadWrite. ALL, Directory. AccessAsUser. ALL</span><span class="sxs-lookup"><span data-stu-id="aa378-112">Application.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>  |
|<span data-ttu-id="aa378-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="aa378-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="aa378-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aa378-114">Not supported.</span></span>    |
|<span data-ttu-id="aa378-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="aa378-115">Application</span></span> | <span data-ttu-id="aa378-116">Application. ReadWrite. Овнедби, Application. ReadWrite. ALL, Directory. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="aa378-116">Application.ReadWrite.OwnedBy, Application.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="aa378-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="aa378-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /servicePrincipals/{id}

```
## <a name="request-headers"></a><span data-ttu-id="aa378-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="aa378-118">Request headers</span></span>
| <span data-ttu-id="aa378-119">Имя</span><span class="sxs-lookup"><span data-stu-id="aa378-119">Name</span></span>       | <span data-ttu-id="aa378-120">Тип</span><span class="sxs-lookup"><span data-stu-id="aa378-120">Type</span></span> | <span data-ttu-id="aa378-121">Описание</span><span class="sxs-lookup"><span data-stu-id="aa378-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="aa378-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="aa378-122">Authorization</span></span>  | <span data-ttu-id="aa378-123">string</span><span class="sxs-lookup"><span data-stu-id="aa378-123">string</span></span>  | <span data-ttu-id="aa378-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="aa378-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="aa378-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="aa378-126">Request body</span></span>
<span data-ttu-id="aa378-127">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="aa378-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="aa378-128">Отклик</span><span class="sxs-lookup"><span data-stu-id="aa378-128">Response</span></span>

<span data-ttu-id="aa378-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="aa378-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="aa378-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="aa378-131">Examples</span></span>
### <a name="request"></a><span data-ttu-id="aa378-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="aa378-132">Request</span></span>
<span data-ttu-id="aa378-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="aa378-133">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_serviceprincipal"
}-->

```http
DELETE https://graph.microsoft.com/beta/servicePrincipals/{id}
```
### <a name="response"></a><span data-ttu-id="aa378-134">Отклик</span><span class="sxs-lookup"><span data-stu-id="aa378-134">Response</span></span>
<span data-ttu-id="aa378-135">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="aa378-135">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Delete servicePrincipal",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
