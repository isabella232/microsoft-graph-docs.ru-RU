---
title: Создание privilegedRoleAssignment
description: Используйте этот интерфейс API для создания нового privilegedRoleAssignment.
ms.openlocfilehash: cee00a71ff9ff233902ba19fb1f3f699ab746f98
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27078716"
---
# <a name="create-privilegedroleassignment"></a><span data-ttu-id="0bbe3-103">Создание privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0bbe3-103">Create privilegedRoleAssignment</span></span>

> <span data-ttu-id="0bbe3-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0bbe3-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0bbe3-106">Используйте этот интерфейс API для создания нового [privilegedRoleAssignment](../resources/privilegedroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="0bbe3-106">Use this API to create a new  [privilegedRoleAssignment](../resources/privilegedroleassignment.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="0bbe3-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="0bbe3-107">Permissions</span></span>
<span data-ttu-id="0bbe3-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0bbe3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="0bbe3-110">Запрашивающая сторона должна иметь роль _Привилегированной роль администратора_ .</span><span class="sxs-lookup"><span data-stu-id="0bbe3-110">The requestor needs to have _Privileged Role Administrator_ role.</span></span> 

|<span data-ttu-id="0bbe3-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="0bbe3-111">Permission type</span></span>      | <span data-ttu-id="0bbe3-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="0bbe3-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0bbe3-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="0bbe3-113">Delegated (work or school account)</span></span> | <span data-ttu-id="0bbe3-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="0bbe3-114">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="0bbe3-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="0bbe3-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0bbe3-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-116">Not supported.</span></span>    |
|<span data-ttu-id="0bbe3-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="0bbe3-117">Application</span></span> | <span data-ttu-id="0bbe3-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0bbe3-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="0bbe3-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedRoleAssignments
```
## <a name="request-headers"></a><span data-ttu-id="0bbe3-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="0bbe3-120">Request headers</span></span>
| <span data-ttu-id="0bbe3-121">Имя</span><span class="sxs-lookup"><span data-stu-id="0bbe3-121">Name</span></span>       | <span data-ttu-id="0bbe3-122">Описание</span><span class="sxs-lookup"><span data-stu-id="0bbe3-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0bbe3-123">Авторизация</span><span class="sxs-lookup"><span data-stu-id="0bbe3-123">Authorization</span></span>  | <span data-ttu-id="0bbe3-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0bbe3-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="0bbe3-126">Request body</span></span>
<span data-ttu-id="0bbe3-127">В тексте запроса укажите представление JSON объекта [privilegedRoleAssignment](../resources/privilegedroleassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="0bbe3-127">In the request body, supply a JSON representation of [privilegedRoleAssignment](../resources/privilegedroleassignment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="0bbe3-128">Ответ</span><span class="sxs-lookup"><span data-stu-id="0bbe3-128">Response</span></span>

<span data-ttu-id="0bbe3-129">Успешно завершена, этот метод возвращает `201 Created` объект [privilegedRoleAssignment](../resources/privilegedroleassignment.md) и кода ответа в теле ответа.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-129">If successful, this method returns `201 Created` response code and [privilegedRoleAssignment](../resources/privilegedroleassignment.md) object in the response body.</span></span>

<span data-ttu-id="0bbe3-130">Обратите внимание, что необходимо зарегистрировать для PIM клиента.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-130">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="0bbe3-131">В противном случае будут возвращены код состояния HTTP 403 запрещено.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-131">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="0bbe3-132">Пример</span><span class="sxs-lookup"><span data-stu-id="0bbe3-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0bbe3-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="0bbe3-133">Request</span></span>
<span data-ttu-id="0bbe3-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="0bbe3-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_privilegedroleassignment_from_privilegedroleassignments"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedRoleAssignments
Content-type: application/json
Content-length: 164

{
  "userId": "userId-value",
  "roleId": "roleId-value"
}
```
<span data-ttu-id="0bbe3-135">В тексте запроса укажите представление JSON объекта [privilegedRoleAssignment](../resources/privilegedroleassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="0bbe3-135">In the request body, supply a JSON representation of [privilegedRoleAssignment](../resources/privilegedroleassignment.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="0bbe3-136">Ответ</span><span class="sxs-lookup"><span data-stu-id="0bbe3-136">Response</span></span>
<span data-ttu-id="0bbe3-p105">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
</span><span class="sxs-lookup"><span data-stu-id="0bbe3-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 184

{
  "id": "id-value",
  "userId": "userId-value",
  "roleId": "roleId-value",
  "isElevated": true,
  "expirationDateTime": "2016-10-19T10:37:00Z",
  "resultMessage": "resultMessage-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create privilegedRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->