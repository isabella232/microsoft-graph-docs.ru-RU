---
title: ОтКлонить riskyUsers
description: Отклонение риска для объекта riskyUsers.
author: cloudhandler
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.date: 03/20/2019
ms.openlocfilehash: 8e7a64e5762808691c4997c83b112a17c9667d47
ms.sourcegitcommit: fd9f62fd9a6d311f98afe2e31afca8b818c402c2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/30/2019
ms.locfileid: "31013133"
---
# <a name="dismiss-riskyusers"></a><span data-ttu-id="b7a0a-103">ОтКлонить riskyUsers</span><span class="sxs-lookup"><span data-stu-id="b7a0a-103">Dismiss riskyUsers</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

><span data-ttu-id="b7a0a-104">**Примечание:** Для использования API riskyUsers требуется лицензия Azure AD Premium P2.</span><span class="sxs-lookup"><span data-stu-id="b7a0a-104">**Note:** Using the riskyUsers API requires an Azure AD Premium P2 license.</span></span>

<span data-ttu-id="b7a0a-105">Отклонение риска для объекта **riskyUsers** .</span><span class="sxs-lookup"><span data-stu-id="b7a0a-105">Dismiss the risk of a **riskyUsers** object.</span></span> <span data-ttu-id="b7a0a-106">Это действие установит для уровня риска целевого пользователя значение нет.</span><span class="sxs-lookup"><span data-stu-id="b7a0a-106">This action will set the targeted user's risk level to none.</span></span>
## <a name="permissions"></a><span data-ttu-id="b7a0a-107">Разрешения</span><span class="sxs-lookup"><span data-stu-id="b7a0a-107">Permissions</span></span>
<span data-ttu-id="b7a0a-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b7a0a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b7a0a-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="b7a0a-110">Permission type</span></span>      | <span data-ttu-id="b7a0a-111">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="b7a0a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b7a0a-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b7a0a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b7a0a-113">Идентитирискюсер. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="b7a0a-113">IdentityRiskyUser.ReadWrite.All</span></span>    |
|<span data-ttu-id="b7a0a-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="b7a0a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b7a0a-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b7a0a-115">Not supported.</span></span>    |
|<span data-ttu-id="b7a0a-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="b7a0a-116">Application</span></span> | <span data-ttu-id="b7a0a-117">Идентитирискюсер. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="b7a0a-117">IdentityRiskyUser.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b7a0a-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="b7a0a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /riskyUsers/dismiss
```


## <a name="request-headers"></a><span data-ttu-id="b7a0a-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="b7a0a-119">Request headers</span></span>
| <span data-ttu-id="b7a0a-120">Имя</span><span class="sxs-lookup"><span data-stu-id="b7a0a-120">Name</span></span>      |<span data-ttu-id="b7a0a-121">Описание</span><span class="sxs-lookup"><span data-stu-id="b7a0a-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="b7a0a-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="b7a0a-122">Authorization</span></span>  | <span data-ttu-id="b7a0a-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b7a0a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b7a0a-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="b7a0a-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="b7a0a-126">Идентификатор сеанса книги, который определяет, сохраняются ли изменения.</span><span class="sxs-lookup"><span data-stu-id="b7a0a-126">Workbook session ID that determines whether changes are persisted.</span></span> <span data-ttu-id="b7a0a-127">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b7a0a-127">Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b7a0a-128">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="b7a0a-128">Request body</span></span>
<span data-ttu-id="b7a0a-129">Укажите идентификаторы пользователя, которые нужно отклонить в теле запроса.</span><span class="sxs-lookup"><span data-stu-id="b7a0a-129">Specify the userIds to dismiss in the request body.</span></span>

## <a name="response"></a><span data-ttu-id="b7a0a-130">Ответ</span><span class="sxs-lookup"><span data-stu-id="b7a0a-130">Response</span></span>

<span data-ttu-id="b7a0a-131">В случае успешного выполнения этот метод возвращает код отклика `204 NoContent`.</span><span class="sxs-lookup"><span data-stu-id="b7a0a-131">If successful, this method returns a `204 NoContent` response code.</span></span>
## <a name="example"></a><span data-ttu-id="b7a0a-132">Пример</span><span class="sxs-lookup"><span data-stu-id="b7a0a-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b7a0a-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="b7a0a-133">Request</span></span>
<span data-ttu-id="b7a0a-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="b7a0a-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "dismiss_riskyuser"
}-->
```http
POST https://graph.microsoft.com/beta/riskyUsers/dismiss

Request Body
{
  "userIds": [
    "04487ee0-f4f6-4e7f-8999-facc5a30e232",
    "13387ee0-f4f6-4e7f-8999-facc5120e345"
  ]
}
```
##### <a name="response"></a><span data-ttu-id="b7a0a-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="b7a0a-135">Response</span></span>
<span data-ttu-id="b7a0a-136">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="b7a0a-136">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.riskyUsers"
} -->
```http
HTTP/1.1 204 NoContent
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Dismiss riskyUsers",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
