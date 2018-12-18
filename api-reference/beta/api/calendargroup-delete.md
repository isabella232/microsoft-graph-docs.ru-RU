---
title: Удаление объекта calendarGroup
description: Удаление группы календарей, отличной от стандартной.
author: angelgolfer-ms
ms.openlocfilehash: edcb75cfe6d395e505a9d100e85bf4e03bde67a8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2018
ms.locfileid: "27336745"
---
# <a name="delete-calendargroup"></a><span data-ttu-id="bbd41-103">Удаление объекта calendarGroup</span><span class="sxs-lookup"><span data-stu-id="bbd41-103">Delete calendarGroup</span></span>

> <span data-ttu-id="bbd41-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="bbd41-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bbd41-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bbd41-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bbd41-106">Удаление группы календарей, отличной от стандартной.</span><span class="sxs-lookup"><span data-stu-id="bbd41-106">Delete a calendar group other than the default calendar group.</span></span>

## <a name="permissions"></a><span data-ttu-id="bbd41-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="bbd41-107">Permissions</span></span>

<span data-ttu-id="bbd41-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bbd41-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="bbd41-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="bbd41-110">Permission type</span></span>                        | <span data-ttu-id="bbd41-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="bbd41-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="bbd41-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="bbd41-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="bbd41-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bbd41-113">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="bbd41-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="bbd41-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bbd41-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bbd41-115">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="bbd41-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="bbd41-116">Application</span></span>                            | <span data-ttu-id="bbd41-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bbd41-117">Calendars.ReadWrite</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="bbd41-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="bbd41-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/calendarGroups/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="bbd41-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="bbd41-119">Request headers</span></span>

| <span data-ttu-id="bbd41-120">Имя</span><span class="sxs-lookup"><span data-stu-id="bbd41-120">Name</span></span>          | <span data-ttu-id="bbd41-121">Тип</span><span class="sxs-lookup"><span data-stu-id="bbd41-121">Type</span></span>   | <span data-ttu-id="bbd41-122">Описание</span><span class="sxs-lookup"><span data-stu-id="bbd41-122">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="bbd41-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bbd41-123">Authorization</span></span> | <span data-ttu-id="bbd41-124">string</span><span class="sxs-lookup"><span data-stu-id="bbd41-124">string</span></span> | <span data-ttu-id="bbd41-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="bbd41-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bbd41-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="bbd41-127">Request body</span></span>

<span data-ttu-id="bbd41-128">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="bbd41-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bbd41-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="bbd41-129">Response</span></span>

<span data-ttu-id="bbd41-p104">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="bbd41-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bbd41-132">Пример</span><span class="sxs-lookup"><span data-stu-id="bbd41-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="bbd41-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="bbd41-133">Request</span></span>

<span data-ttu-id="bbd41-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="bbd41-134">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_calendargroup"
}-->

```http
DELETE https://graph.microsoft.com/beta/me/calendarGroups/{id}
```

##### <a name="response"></a><span data-ttu-id="bbd41-135">Ответ</span><span class="sxs-lookup"><span data-stu-id="bbd41-135">Response</span></span>

<span data-ttu-id="bbd41-p105">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="bbd41-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
