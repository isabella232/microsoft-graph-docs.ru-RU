---
title: Создание группы маршрутизации звука
description: Создание нового **аудиораутингграуп**.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: fc3f32592bb466bf345734cdd924472fe245730c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35438666"
---
# <a name="create-audio-routing-group"></a><span data-ttu-id="c0d8f-103">Создание группы маршрутизации звука</span><span class="sxs-lookup"><span data-stu-id="c0d8f-103">Create audio routing group</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="c0d8f-104">Создание нового **аудиораутингграуп**.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-104">Create a new **audioRoutingGroup**.</span></span>

## <a name="permissions"></a><span data-ttu-id="c0d8f-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="c0d8f-105">Permissions</span></span>
<span data-ttu-id="c0d8f-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c0d8f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="c0d8f-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="c0d8f-108">Permission type</span></span>                        | <span data-ttu-id="c0d8f-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="c0d8f-109">Permissions (from least to most privileged)</span></span> |
|:---------------------------------------|:--------------------------------------------|
| <span data-ttu-id="c0d8f-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c0d8f-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="c0d8f-111">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-111">Not supported.</span></span>                               |
| <span data-ttu-id="c0d8f-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="c0d8f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c0d8f-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-113">Not supported.</span></span>                               |
| <span data-ttu-id="c0d8f-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="c0d8f-114">Application</span></span>                            | <span data-ttu-id="c0d8f-115">Calls. Жоинграупкаллс. ALL, Calls. Инитиатеграупкаллс. ALL</span><span class="sxs-lookup"><span data-stu-id="c0d8f-115">Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c0d8f-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="c0d8f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/audioRoutingGroups
POST /applications/{id}/calls/{id}/audioRoutingGroups
```

## <a name="request-headers"></a><span data-ttu-id="c0d8f-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="c0d8f-117">Request headers</span></span>
| <span data-ttu-id="c0d8f-118">Имя</span><span class="sxs-lookup"><span data-stu-id="c0d8f-118">Name</span></span>          | <span data-ttu-id="c0d8f-119">Описание</span><span class="sxs-lookup"><span data-stu-id="c0d8f-119">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="c0d8f-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="c0d8f-120">Authorization</span></span> | <span data-ttu-id="c0d8f-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c0d8f-123">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="c0d8f-123">Request body</span></span>
<span data-ttu-id="c0d8f-124">В тексте запроса добавьте представление объекта [аудиораутингграуп](../resources/audioroutinggroup.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-124">In the request body, supply a JSON representation of [audioRoutingGroup](../resources/audioroutinggroup.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="c0d8f-125">Отклик</span><span class="sxs-lookup"><span data-stu-id="c0d8f-125">Response</span></span>
<span data-ttu-id="c0d8f-126">В случае успешного выполнения этот метод `200 OK` возвращает код отклика и объект [аудиораутингграуп](../resources/audioroutinggroup.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-126">If successful, this method returns `200 OK` response code and [audioRoutingGroup](../resources/audioroutinggroup.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="c0d8f-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="c0d8f-127">Examples</span></span>

### <a name="example-1-one-to-one-audio-routing-group"></a><span data-ttu-id="c0d8f-128">Пример 1: "одна к одной группе маршрутизации аудио"</span><span class="sxs-lookup"><span data-stu-id="c0d8f-128">Example 1: One-to-one audio routing group</span></span>

##### <a name="request"></a><span data-ttu-id="c0d8f-129">Запрос</span><span class="sxs-lookup"><span data-stu-id="c0d8f-129">Request</span></span>
<span data-ttu-id="c0d8f-130">Ниже показан пример запроса.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-130">The following example shows the request.</span></span>


# <a name="httptabhttp"></a>[<span data-ttu-id="c0d8f-131">HTTP</span><span class="sxs-lookup"><span data-stu-id="c0d8f-131">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create-audioRoutingGroup-from-call"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/audioRoutingGroups
Content-Type: application/json
Content-Length: 233

{
  "id": "oneToOne",
  "routingMode": "oneToOne",
  "sources": [
    "632899f8-2ea1-4604-8413-27bd2892079f"
  ],
  "receivers": [
    "550fae72-d251-43ec-868c-373732c2704f"
  ]
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="c0d8f-132">C#</span><span class="sxs-lookup"><span data-stu-id="c0d8f-132">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-audioroutinggroup-from-call-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="c0d8f-133">Javascript</span><span class="sxs-lookup"><span data-stu-id="c0d8f-133">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-audioroutinggroup-from-call-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="c0d8f-134">Цель — C</span><span class="sxs-lookup"><span data-stu-id="c0d8f-134">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-audioroutinggroup-from-call-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


<span data-ttu-id="c0d8f-135">В тексте запроса добавьте представление объекта [аудиораутингграуп](../resources/audioroutinggroup.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-135">In the request body, supply a JSON representation of [audioRoutingGroup](../resources/audioroutinggroup.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="c0d8f-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="c0d8f-136">Response</span></span>

> <span data-ttu-id="c0d8f-p103">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.audioRoutingGroup"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 233

{
  "id": "oneToOne",
  "routingMode": "oneToOne",
  "sources": [
    "632899f8-2ea1-4604-8413-27bd2892079f"
  ],
  "receivers": [
    "550fae72-d251-43ec-868c-373732c2704f"
  ]
}
```
### <a name="example-2-multicast-audioroutinggroup"></a><span data-ttu-id="c0d8f-139">Пример 2: multicast Аудиораутингграуп</span><span class="sxs-lookup"><span data-stu-id="c0d8f-139">Example 2: Multicast audioRoutingGroup</span></span>

##### <a name="request"></a><span data-ttu-id="c0d8f-140">Запрос</span><span class="sxs-lookup"><span data-stu-id="c0d8f-140">Request</span></span>
<span data-ttu-id="c0d8f-141">Ниже показан пример запроса.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-141">The following example shows the request.</span></span>

```http
POST https://graph.microsoft.com/beta/app/calls/{id}/audioRoutingGroups
Content-Type: application/json
Content-Length: 233
```

<!-- {
  "blockType": "example",
  "name": "create-audioRoutingGroup-from-call",
  "@odata.type": "microsoft.graph.audioRoutingGroup"
}-->

```json
{
  "id": "multicast",
  "routingMode": "multicast",
  "sources": [
    "632899f8-2ea1-4604-8413-27bd2892079f"
  ],
  "receivers": [
    "550fae72-d251-43ec-868c-373732c2704f",
    "72f988bf-86f1-41af-91ab-2d7cd011db47"
  ]
}
```

<span data-ttu-id="c0d8f-142">В тексте запроса добавьте представление объекта [аудиораутингграуп](../resources/audioroutinggroup.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-142">In the request body, supply a JSON representation of [audioRoutingGroup](../resources/audioroutinggroup.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="c0d8f-143">Отклик</span><span class="sxs-lookup"><span data-stu-id="c0d8f-143">Response</span></span>

> <span data-ttu-id="c0d8f-p104">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="c0d8f-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 233
```
<!-- {
  "blockType": "example",
  "truncated": true,
  "@odata.type": "microsoft.graph.audioRoutingGroup"
} -->

```json
{
  "id": "multicast",
  "routingMode": "multicast",
  "sources": [
    "632899f8-2ea1-4604-8413-27bd2892079f"
  ],
  "receivers": [
    "550fae72-d251-43ec-868c-373732c2704f",
    "72f988bf-86f1-41af-91ab-2d7cd011db47"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create audioRoutingGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
