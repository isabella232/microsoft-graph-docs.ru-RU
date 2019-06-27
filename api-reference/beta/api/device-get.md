---
title: Получение устройства
description: Получение свойств и связей объекта устройства.
author: davidmu1
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: d6bf4e1060c723c1cba9d77811d76f8be20518bc
ms.sourcegitcommit: 0e1101d499f35b08aa2309e273871438b1774979
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2019
ms.locfileid: "35261014"
---
# <a name="get-device"></a><span data-ttu-id="706a4-103">Получение устройства</span><span class="sxs-lookup"><span data-stu-id="706a4-103">Get device</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="706a4-104">Получение свойств и связей объекта устройства.</span><span class="sxs-lookup"><span data-stu-id="706a4-104">Get the properties and relationships of a device object.</span></span>

<span data-ttu-id="706a4-105">Так как ресурс **Device** поддерживает [расширения](/graph/extensibility-overview), с помощью `GET` операции можно также получить настраиваемые свойства и данные расширения в экземпляре **устройства** .</span><span class="sxs-lookup"><span data-stu-id="706a4-105">Since the **device** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in a **device** instance.</span></span>

## <a name="permissions"></a><span data-ttu-id="706a4-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="706a4-106">Permissions</span></span>
<span data-ttu-id="706a4-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="706a4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="706a4-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="706a4-109">Permission type</span></span>      | <span data-ttu-id="706a4-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="706a4-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="706a4-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="706a4-111">Delegated (work or school account)</span></span> | <span data-ttu-id="706a4-112">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="706a4-112">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="706a4-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="706a4-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="706a4-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="706a4-114">Not supported.</span></span>    |
|<span data-ttu-id="706a4-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="706a4-115">Application</span></span> | <span data-ttu-id="706a4-116">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="706a4-116">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="706a4-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="706a4-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="706a4-118">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="706a4-118">Optional query parameters</span></span>
<span data-ttu-id="706a4-119">Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.</span><span class="sxs-lookup"><span data-stu-id="706a4-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="706a4-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="706a4-120">Request headers</span></span>
| <span data-ttu-id="706a4-121">Имя</span><span class="sxs-lookup"><span data-stu-id="706a4-121">Name</span></span>       | <span data-ttu-id="706a4-122">Тип</span><span class="sxs-lookup"><span data-stu-id="706a4-122">Type</span></span> | <span data-ttu-id="706a4-123">Описание</span><span class="sxs-lookup"><span data-stu-id="706a4-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="706a4-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="706a4-124">Authorization</span></span>  | <span data-ttu-id="706a4-125">string</span><span class="sxs-lookup"><span data-stu-id="706a4-125">string</span></span>  | <span data-ttu-id="706a4-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="706a4-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="706a4-128">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="706a4-128">Request body</span></span>
<span data-ttu-id="706a4-129">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="706a4-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="706a4-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="706a4-130">Response</span></span>

<span data-ttu-id="706a4-131">В случае успеха этот метод возвращает код отклика `200 OK` и объект [device](../resources/device.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="706a4-131">If successful, this method returns a `200 OK` response code and [device](../resources/device.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="706a4-132">Пример</span><span class="sxs-lookup"><span data-stu-id="706a4-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="706a4-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="706a4-133">Request</span></span>
<span data-ttu-id="706a4-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="706a4-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_device"
}-->
```http
GET https://graph.microsoft.com/beta/devices/{id}
```

> <span data-ttu-id="706a4-135">Примечание. Параметр id в запросе — это свойство id объекта device, а не свойство deviceId.</span><span class="sxs-lookup"><span data-stu-id="706a4-135">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

##### <a name="response"></a><span data-ttu-id="706a4-136">Отклик</span><span class="sxs-lookup"><span data-stu-id="706a4-136">Response</span></span>
<span data-ttu-id="706a4-p103">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="706a4-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 322

{
  "accountEnabled": true,
  "approximateLastSignInDateTime": "2016-10-19T10:37:00Z",
  "deviceId": "deviceId-value",
  "deviceMetadata": "deviceMetadata-value",
  "deviceVersion": 99
}
```
#### <a name="sdk-sample-code"></a><span data-ttu-id="706a4-140">Пример кода SDK</span><span class="sxs-lookup"><span data-stu-id="706a4-140">SDK sample code</span></span>
# <a name="ctabcs"></a>[<span data-ttu-id="706a4-141">C#</span><span class="sxs-lookup"><span data-stu-id="706a4-141">C#</span></span>](#tab/cs)
[!INCLUDE [sample-code](../includes/get_device-Cs-snippets.md)]

# <a name="javascripttabjavascript"></a>[<span data-ttu-id="706a4-142">Javascript</span><span class="sxs-lookup"><span data-stu-id="706a4-142">Javascript</span></span>](#tab/javascript)
[!INCLUDE [sample-code](../includes/get_device-Javascript-snippets.md)]

# <a name="objective-ctabobjective-c"></a>[<span data-ttu-id="706a4-143">Цель — C</span><span class="sxs-lookup"><span data-stu-id="706a4-143">Objective-C</span></span>](#tab/objective-c)
[!INCLUDE [sample-code](../includes/get_device-Objective-C-snippets.md)]
---

[!INCLUDE [sdk-documentation](../includes/snippets_sdk_documentation_link.md)]

## <a name="see-also"></a><span data-ttu-id="706a4-144">См. также</span><span class="sxs-lookup"><span data-stu-id="706a4-144">See also</span></span>

- [<span data-ttu-id="706a4-145">Добавление пользовательских данных в ресурсы с помощью расширений</span><span class="sxs-lookup"><span data-stu-id="706a4-145">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="706a4-146">Добавление пользовательских данных в ресурсы user с помощью открытых расширений (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="706a4-146">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="706a4-147">Добавление пользовательских данных в ресурсы group с помощью расширений схемы (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="706a4-147">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Get device",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/device-get.md:\r\n      BookmarkMissing: '[#tab/objective-c](Objective-C)'. Did you mean: #objective-c (score: 4)",
    "Error: /api-reference/beta/api/device-get.md:\r\n      BookmarkMissing: '[#tab/cs](C#)'. Did you mean: #c (score: 5)",
    "Error: /api-reference/beta/api/device-get.md:\r\n      BookmarkMissing: '[#tab/javascript](Javascript)'. Did you mean: #javascript (score: 4)"
  ]
}
-->
