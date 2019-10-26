---
title: Удаление Усерфлов
description: Удаление Усерфлов.
localization_priority: Normal
author: valnav
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 174cc8324b58c3a4deb627cd6f40bcbbab31f6a3
ms.sourcegitcommit: 8bef2bc8b9e56d1a787ea2f0cda4ed94f05109ad
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/26/2019
ms.locfileid: "37734681"
---
# <a name="delete-userflow"></a><span data-ttu-id="6219b-103">Удаление Усерфлов</span><span class="sxs-lookup"><span data-stu-id="6219b-103">Delete userFlow</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="6219b-104">Удаление существующего объекта [усерфлов](../resources/identityuserflow.md) .</span><span class="sxs-lookup"><span data-stu-id="6219b-104">Delete an existing [userFlow](../resources/identityuserflow.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="6219b-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="6219b-105">Permissions</span></span>

<span data-ttu-id="6219b-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6219b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="6219b-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="6219b-108">Permission type</span></span>                        | <span data-ttu-id="6219b-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="6219b-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="6219b-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6219b-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="6219b-111">Идентитюсерфлов. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="6219b-111">IdentityUserFlow.ReadWrite.All</span></span> |
| <span data-ttu-id="6219b-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="6219b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6219b-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6219b-113">Not supported.</span></span> |
| <span data-ttu-id="6219b-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="6219b-114">Application</span></span>                            | <span data-ttu-id="6219b-115">Идентитюсерфлов. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="6219b-115">IdentityUserFlow.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6219b-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="6219b-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /identity/userFlows/{id}
```

## <a name="request-headers"></a><span data-ttu-id="6219b-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="6219b-117">Request headers</span></span>

| <span data-ttu-id="6219b-118">Имя</span><span class="sxs-lookup"><span data-stu-id="6219b-118">Name</span></span>          | <span data-ttu-id="6219b-119">Описание</span><span class="sxs-lookup"><span data-stu-id="6219b-119">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="6219b-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="6219b-120">Authorization</span></span> | <span data-ttu-id="6219b-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6219b-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6219b-123">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="6219b-123">Request body</span></span>

<span data-ttu-id="6219b-124">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="6219b-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6219b-125">Отклик</span><span class="sxs-lookup"><span data-stu-id="6219b-125">Response</span></span>

<span data-ttu-id="6219b-p103">При успешном выполнении этот метод возвращает код отклика `204 No Content`. Метод не возвращает данные в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="6219b-p103">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="6219b-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="6219b-128">Examples</span></span>

### <a name="request"></a><span data-ttu-id="6219b-129">Запрос</span><span class="sxs-lookup"><span data-stu-id="6219b-129">Request</span></span>

<span data-ttu-id="6219b-130">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="6219b-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_identityuserflow"
}-->

```http
DELETE https://graph.microsoft.com/beta/identity/userFlows/{id}
```

### <a name="response"></a><span data-ttu-id="6219b-131">Отклик</span><span class="sxs-lookup"><span data-stu-id="6219b-131">Response</span></span>

<span data-ttu-id="6219b-132">Ниже приведен пример ответа.</span><span class="sxs-lookup"><span data-stu-id="6219b-132">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete userFlow",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->