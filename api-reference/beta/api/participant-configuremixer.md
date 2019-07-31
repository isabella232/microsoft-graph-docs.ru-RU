---
title: 'участник: Конфигуремиксер'
description: Настройка смешанного звука для разных участников многочастной беседы.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: dc3bb039fa005d83738d8fd0a762a465c092048b
ms.sourcegitcommit: 2c62457e57467b8d50f21b255b553106a9a5d8d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2019
ms.locfileid: "35992467"
---
# <a name="participant-configuremixer"></a><span data-ttu-id="f6704-103">участник: Конфигуремиксер</span><span class="sxs-lookup"><span data-stu-id="f6704-103">participant: configureMixer</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="f6704-104">Настройка смешанного звука для разных участников многочастной беседы.</span><span class="sxs-lookup"><span data-stu-id="f6704-104">Configure how audio is mixed for different participants in a multiparty conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="f6704-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="f6704-105">Permissions</span></span>
<span data-ttu-id="f6704-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f6704-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="f6704-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="f6704-108">Permission type</span></span> | <span data-ttu-id="f6704-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="f6704-109">Permissions (from least to most privileged)</span></span> |
| :-------------- | :------------------------------------------ |
| <span data-ttu-id="f6704-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="f6704-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="f6704-111">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6704-111">Not Supported</span></span>        |
| <span data-ttu-id="f6704-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="f6704-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f6704-113">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6704-113">Not Supported</span></span>        |
| <span data-ttu-id="f6704-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="f6704-114">Application</span></span>     | <span data-ttu-id="f6704-115">Calls. Жоинграупкаллс. ALL, Calls. Инитиатеграупкаллс. ALL</span><span class="sxs-lookup"><span data-stu-id="f6704-115">Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f6704-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="f6704-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/participants/configureMixer
POST /applications/{id}/calls/{id}/participants/configureMixer
```

## <a name="request-headers"></a><span data-ttu-id="f6704-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="f6704-117">Request headers</span></span>
| <span data-ttu-id="f6704-118">Имя</span><span class="sxs-lookup"><span data-stu-id="f6704-118">Name</span></span>          | <span data-ttu-id="f6704-119">Описание</span><span class="sxs-lookup"><span data-stu-id="f6704-119">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="f6704-120">Авторизация</span><span class="sxs-lookup"><span data-stu-id="f6704-120">Authorization</span></span> | <span data-ttu-id="f6704-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="f6704-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f6704-123">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="f6704-123">Request body</span></span>
<span data-ttu-id="f6704-124">В тексте запроса предоставьте JSON-объект с указанными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="f6704-124">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f6704-125">Параметр</span><span class="sxs-lookup"><span data-stu-id="f6704-125">Parameter</span></span>      | <span data-ttu-id="f6704-126">Тип</span><span class="sxs-lookup"><span data-stu-id="f6704-126">Type</span></span>    |<span data-ttu-id="f6704-127">Описание</span><span class="sxs-lookup"><span data-stu-id="f6704-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f6704-128">ПартиЦипантмиксерлевелс</span><span class="sxs-lookup"><span data-stu-id="f6704-128">participantMixerLevels</span></span>|<span data-ttu-id="f6704-129">Коллекция [партиЦипантмиксерлевел](../resources/participantmixerlevel.md)</span><span class="sxs-lookup"><span data-stu-id="f6704-129">[participantMixerLevel](../resources/participantmixerlevel.md) collection</span></span>| <span data-ttu-id="f6704-130">Настройка уровней микшера для данного участника аудио.</span><span class="sxs-lookup"><span data-stu-id="f6704-130">Configuration of mixer levels for given audio participant.</span></span>|
|<span data-ttu-id="f6704-131">Контекст</span><span class="sxs-lookup"><span data-stu-id="f6704-131">clientContext</span></span>|<span data-ttu-id="f6704-132">String</span><span class="sxs-lookup"><span data-stu-id="f6704-132">String</span></span>|<span data-ttu-id="f6704-133">Контекст клиента.</span><span class="sxs-lookup"><span data-stu-id="f6704-133">The client context.</span></span>|

## <a name="response"></a><span data-ttu-id="f6704-134">Отклик</span><span class="sxs-lookup"><span data-stu-id="f6704-134">Response</span></span>
<span data-ttu-id="f6704-135">Возвращает `202 Accepted` код отклика и заголовок Location с URI для [коммсоператион](../resources/commsoperation.md) , созданного для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="f6704-135">Returns `202 Accepted` response code and a Location header with a uri to the [commsOperation](../resources/commsoperation.md) created for this request.</span></span>

## <a name="example"></a><span data-ttu-id="f6704-136">Пример</span><span class="sxs-lookup"><span data-stu-id="f6704-136">Example</span></span>
<span data-ttu-id="f6704-137">В приведенном ниже примере показано, как вызывать этот API.</span><span class="sxs-lookup"><span data-stu-id="f6704-137">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="f6704-138">Запрос</span><span class="sxs-lookup"><span data-stu-id="f6704-138">Request</span></span>
<span data-ttu-id="f6704-139">Ниже показан пример запроса.</span><span class="sxs-lookup"><span data-stu-id="f6704-139">The following example shows the request.</span></span>


# <a name="httptabhttp"></a>[<span data-ttu-id="f6704-140">HTTP</span><span class="sxs-lookup"><span data-stu-id="f6704-140">HTTP</span></span>](#tab/http)
<!-- {
  "blockType": "request",
  "name": "participant-configureMixer"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/participants/configureMixer
Content-Type: application/json
Content-Length: 501

{
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
  "participantMixerLevels": [
    {
      "participant": "550fae72-d251-43ec-868c-373732c2704f",
      "exclusive": true,
      "ducking": {
        "rampActive": 50,
        "rampInactive": 50,
        "lowerLevel": 10,
        "upperLevel": 50
      },
      "sourceLevels": [
        {
          "participant": "632899f8-2ea1-4604-8413-27bd2892079f",
          "level": 50,
          "duckOthers": false
        }
      ]
    }
  ]
}
```
# <a name="ctabcsharp"></a>[<span data-ttu-id="f6704-141">C#</span><span class="sxs-lookup"><span data-stu-id="f6704-141">C#</span></span>](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/participant-configuremixer-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="f6704-142">Javascript</span><span class="sxs-lookup"><span data-stu-id="f6704-142">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/participant-configuremixer-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[<span data-ttu-id="f6704-143">Цель — C</span><span class="sxs-lookup"><span data-stu-id="f6704-143">Objective-C</span></span>](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/participant-configuremixer-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[<span data-ttu-id="f6704-144">Java</span><span class="sxs-lookup"><span data-stu-id="f6704-144">Java</span></span>](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/participant-configuremixer-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a><span data-ttu-id="f6704-145">Отклик</span><span class="sxs-lookup"><span data-stu-id="f6704-145">Response</span></span>

> <span data-ttu-id="f6704-p103">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="f6704-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.commsOperation"
} -->
```http
HTTP/1.1 202 Accepted
Location: https://graph.microsoft.com/beta/app/calls/57dab8b1-894c-409a-b240-bd8beae78896/operations/0fe0623f-d628-42ed-b4bd-8ac290072cc5
```

##### <a name="notification---operation-completed"></a><span data-ttu-id="f6704-148">Уведомление о завершении операции</span><span class="sxs-lookup"><span data-stu-id="f6704-148">Notification - operation completed</span></span>

```http
POST https://bot.contoso.com/api/calls
Authorization: Bearer <TOKEN>
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "value": [
    {
      "changeType": "deleted",
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/operations/0FE0623FD62842EDB4BD8AC290072CC5",
      "resourceData": {
        "@odata.type": "#microsoft.graph.commsOperation",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/operations/0FE0623FD62842EDB4BD8AC290072CC5",
        "@odata.etag": "W/\"1\"",
        "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
        "status": "completed"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "participant: configureMixer",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
