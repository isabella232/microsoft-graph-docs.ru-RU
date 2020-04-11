---
title: Назначение типа ресурса tokenLifetimePolicy
description: Назначьте Токенлифетимеполици приложению.
localization_priority: Normal
author: sureshja
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: a9d6b917ac9e819371ab5d91f379c7d69621665b
ms.sourcegitcommit: 9a6ce4ddf75beead19b7c35a1949cf4d105b9b29
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/11/2020
ms.locfileid: "43229213"
---
# <a name="assign-tokenlifetimepolicy"></a><span data-ttu-id="cd449-103">Назначение типа ресурса tokenLifetimePolicy</span><span class="sxs-lookup"><span data-stu-id="cd449-103">Assign tokenLifetimePolicy</span></span>

<span data-ttu-id="cd449-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="cd449-104">Namespace: microsoft.graph</span></span>



<span data-ttu-id="cd449-105">Назначьте [токенлифетимеполици](../resources/tokenlifetimepolicy.md) [приложению](../resources/application.md).</span><span class="sxs-lookup"><span data-stu-id="cd449-105">Assign a [tokenLifetimePolicy](../resources/tokenlifetimepolicy.md) to an [application](../resources/application.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="cd449-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="cd449-106">Permissions</span></span>

<span data-ttu-id="cd449-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cd449-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="cd449-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="cd449-109">Permission type</span></span>                        | <span data-ttu-id="cd449-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="cd449-110">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="cd449-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="cd449-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="cd449-112">Policy. Read. ALL и Application. ReadWrite. ALL, Policy. ReadWrite. Аппликатионконфигуратион и Application. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="cd449-112">Policy.Read.All and Application.ReadWrite.All, Policy.ReadWrite.ApplicationConfiguration and Application.ReadWrite.All</span></span> |
| <span data-ttu-id="cd449-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="cd449-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cd449-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd449-114">Not supported.</span></span> |
| <span data-ttu-id="cd449-115">Приложение</span><span class="sxs-lookup"><span data-stu-id="cd449-115">Application</span></span>                            | <span data-ttu-id="cd449-116">Policy. Read. ALL и Application. ReadWrite. Овнедби, Policy. Read. ALL и Application. ReadWrite. ALL, Policy. ReadWrite. Аппликатионконфигуратион и Application. ReadWrite. Овнедби, Policy. ReadWrite. Аппликатионконфигуратион и Application. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="cd449-116">Policy.Read.All and Application.ReadWrite.OwnedBy, Policy.Read.All and Application.ReadWrite.All, Policy.ReadWrite.ApplicationConfiguration and Application.ReadWrite.OwnedBy, Policy.ReadWrite.ApplicationConfiguration and Application.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cd449-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="cd449-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /applications/{id}/tokenLifetimePolicies/$ref
```

## <a name="request-headers"></a><span data-ttu-id="cd449-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="cd449-118">Request headers</span></span>

| <span data-ttu-id="cd449-119">Имя</span><span class="sxs-lookup"><span data-stu-id="cd449-119">Name</span></span>          | <span data-ttu-id="cd449-120">Описание</span><span class="sxs-lookup"><span data-stu-id="cd449-120">Description</span></span>   |
|:--------------|:--------------|
| <span data-ttu-id="cd449-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="cd449-121">Authorization</span></span> | <span data-ttu-id="cd449-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="cd449-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="cd449-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="cd449-124">Content-Type</span></span> | <span data-ttu-id="cd449-p103">application/json. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="cd449-p103">application/json. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cd449-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="cd449-127">Request body</span></span>

<span data-ttu-id="cd449-128">В тексте запроса укажите идентификатор объекта [токенлифетимеполици](../resources/tokenlifetimepolicy.md) (с помощью `@odata.id` свойства), который должен быть назначен для приложения или участника-службы.</span><span class="sxs-lookup"><span data-stu-id="cd449-128">In the request body, supply the identifier of the [tokenLifetimePolicy](../resources/tokenlifetimepolicy.md) object (using an `@odata.id` property) that should be assigned to the application or service principal.</span></span>

## <a name="response"></a><span data-ttu-id="cd449-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="cd449-129">Response</span></span>

<span data-ttu-id="cd449-p104">При успешном выполнении этот метод возвращает код отклика `204 No Content`. Метод не возвращает данные в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="cd449-p104">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="cd449-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="cd449-132">Examples</span></span>

### <a name="request"></a><span data-ttu-id="cd449-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="cd449-133">Request</span></span>

<span data-ttu-id="cd449-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="cd449-134">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_tokenlifetimepolicy_from_application"
}-->

```http
POST https://graph.microsoft.com/v1.0/applications/{id}/tokenLifetimePolicies/$ref
Content-Type: application/json

{
  "@odata.id":"https://graph.microsoft.com/v1.0/policies/tokenLifetimePolicies/cd3d9b57-0aee-4f25-8ee3-ac74ef5986a9"
}
```

### <a name="response"></a><span data-ttu-id="cd449-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="cd449-135">Response</span></span>

<span data-ttu-id="cd449-136">Ниже приведен пример ответа.</span><span class="sxs-lookup"><span data-stu-id="cd449-136">The following is an example of the response.</span></span>

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
  "description": "Assign tokenLifetimePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
