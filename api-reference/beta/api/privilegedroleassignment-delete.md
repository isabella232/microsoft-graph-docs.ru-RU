---
title: Удаление privilegedRoleAssignment
description: Удалите privilegedRoleAssignment.
ms.openlocfilehash: 345ebbfbf32a8d5e6f9399e5746ca9ece9b91d3b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27076094"
---
# <a name="delete-privilegedroleassignment"></a><span data-ttu-id="74ea3-103">Удаление privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="74ea3-103">Delete privilegedRoleAssignment</span></span>

> <span data-ttu-id="74ea3-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="74ea3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="74ea3-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="74ea3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="74ea3-106">Удалите [privilegedRoleAssignment](../resources/privilegedroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="74ea3-106">Delete [privilegedRoleAssignment](../resources/privilegedroleassignment.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="74ea3-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="74ea3-107">Permissions</span></span>
<span data-ttu-id="74ea3-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="74ea3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="74ea3-110">Запрашивающая сторона должна иметь роль _Привилегированной роль администратора_ .</span><span class="sxs-lookup"><span data-stu-id="74ea3-110">The requestor needs to have _Privileged Role Administrator_ role.</span></span>
 

|<span data-ttu-id="74ea3-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="74ea3-111">Permission type</span></span>      | <span data-ttu-id="74ea3-112">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="74ea3-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="74ea3-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="74ea3-113">Delegated (work or school account)</span></span> | <span data-ttu-id="74ea3-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="74ea3-114">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="74ea3-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="74ea3-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="74ea3-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="74ea3-116">Not supported.</span></span>    |
|<span data-ttu-id="74ea3-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="74ea3-117">Application</span></span> | <span data-ttu-id="74ea3-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="74ea3-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="74ea3-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="74ea3-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /privilegedRoleAssignments/{id}
```

<span data-ttu-id="74ea3-120">Обратите внимание, что ``<id>`` в формате «userId_roleId», где идентификатор пользователя — это строка идентификатора GUID для Azure AD идентификатор пользователя, а roleId — string GUID для идентификатора роль Azure администратора.</span><span class="sxs-lookup"><span data-stu-id="74ea3-120">Note that ``<id>`` is in the format of 'userId_roleId', where userId is the GUID string for Azure AD user id, and roleId is the GUID string for Azure administrator role id.</span></span>

## <a name="request-headers"></a><span data-ttu-id="74ea3-121">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="74ea3-121">Request headers</span></span>
| <span data-ttu-id="74ea3-122">Имя</span><span class="sxs-lookup"><span data-stu-id="74ea3-122">Name</span></span>       | <span data-ttu-id="74ea3-123">Описание</span><span class="sxs-lookup"><span data-stu-id="74ea3-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="74ea3-124">Авторизация</span><span class="sxs-lookup"><span data-stu-id="74ea3-124">Authorization</span></span>  | <span data-ttu-id="74ea3-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="74ea3-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="74ea3-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="74ea3-127">Request body</span></span>
<span data-ttu-id="74ea3-128">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="74ea3-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="74ea3-129">Отклик</span><span class="sxs-lookup"><span data-stu-id="74ea3-129">Response</span></span>

<span data-ttu-id="74ea3-p104">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="74ea3-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

<span data-ttu-id="74ea3-132">Обратите внимание, что необходимо зарегистрировать для PIM клиента.</span><span class="sxs-lookup"><span data-stu-id="74ea3-132">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="74ea3-133">В противном случае будут возвращены код состояния HTTP 403 запрещено.</span><span class="sxs-lookup"><span data-stu-id="74ea3-133">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="74ea3-134">Пример</span><span class="sxs-lookup"><span data-stu-id="74ea3-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="74ea3-135">Запрос</span><span class="sxs-lookup"><span data-stu-id="74ea3-135">Request</span></span>
<span data-ttu-id="74ea3-136">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="74ea3-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_privilegedroleassignment"
}-->
```http
DELETE https://graph.microsoft.com/beta/privilegedRoleAssignments/{id}
```
##### <a name="response"></a><span data-ttu-id="74ea3-137">Ответ</span><span class="sxs-lookup"><span data-stu-id="74ea3-137">Response</span></span>
<span data-ttu-id="74ea3-p106">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
</span><span class="sxs-lookup"><span data-stu-id="74ea3-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete privilegedRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->