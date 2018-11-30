---
title: Удаление объекта calendarGroup
description: Удаление группы календарей, отличной от стандартной.
ms.openlocfilehash: 64fa9069ba54c7549392db4fc2d3d47b4e95ebdc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27026149"
---
# <a name="delete-calendargroup"></a><span data-ttu-id="d1b06-103">Удаление объекта calendarGroup</span><span class="sxs-lookup"><span data-stu-id="d1b06-103">Delete calendarGroup</span></span>

<span data-ttu-id="d1b06-104">Удаление группы календарей, отличной от стандартной.</span><span class="sxs-lookup"><span data-stu-id="d1b06-104">Delete a calendar group other than the default calendar group.</span></span>

## <a name="permissions"></a><span data-ttu-id="d1b06-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="d1b06-105">Permissions</span></span>

<span data-ttu-id="d1b06-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d1b06-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="d1b06-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="d1b06-108">Permission type</span></span>                        | <span data-ttu-id="d1b06-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="d1b06-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="d1b06-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d1b06-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="d1b06-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1b06-111">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="d1b06-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="d1b06-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d1b06-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1b06-113">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="d1b06-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="d1b06-114">Application</span></span>                            | <span data-ttu-id="d1b06-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1b06-115">Calendars.ReadWrite</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="d1b06-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="d1b06-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/calendarGroups/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="d1b06-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="d1b06-117">Request headers</span></span>

| <span data-ttu-id="d1b06-118">Имя</span><span class="sxs-lookup"><span data-stu-id="d1b06-118">Name</span></span>          | <span data-ttu-id="d1b06-119">Тип</span><span class="sxs-lookup"><span data-stu-id="d1b06-119">Type</span></span>   | <span data-ttu-id="d1b06-120">Описание</span><span class="sxs-lookup"><span data-stu-id="d1b06-120">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="d1b06-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="d1b06-121">Authorization</span></span> | <span data-ttu-id="d1b06-122">string</span><span class="sxs-lookup"><span data-stu-id="d1b06-122">string</span></span> | <span data-ttu-id="d1b06-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d1b06-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d1b06-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="d1b06-125">Request body</span></span>

<span data-ttu-id="d1b06-126">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="d1b06-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d1b06-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="d1b06-127">Response</span></span>

<span data-ttu-id="d1b06-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="d1b06-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d1b06-130">Пример</span><span class="sxs-lookup"><span data-stu-id="d1b06-130">Example</span></span>

##### <a name="request"></a><span data-ttu-id="d1b06-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="d1b06-131">Request</span></span>

<span data-ttu-id="d1b06-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="d1b06-132">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_calendargroup"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
```

##### <a name="response"></a><span data-ttu-id="d1b06-133">Ответ</span><span class="sxs-lookup"><span data-stu-id="d1b06-133">Response</span></span>

<span data-ttu-id="d1b06-p104">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
</span><span class="sxs-lookup"><span data-stu-id="d1b06-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "Delete calendarGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
