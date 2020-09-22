---
title: Обновление вкладки
description: Обновление свойств указанной вкладки.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: 844af5873d621a2826b2f4291d228196424fd6b0
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47978281"
---
# <a name="update-tab"></a><span data-ttu-id="851ef-103">Обновление вкладки</span><span class="sxs-lookup"><span data-stu-id="851ef-103">Update tab</span></span>

<span data-ttu-id="851ef-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="851ef-104">Namespace: microsoft.graph</span></span>


<span data-ttu-id="851ef-105">Обновление свойств указанной [вкладки](../resources/teamstab.md). Это можно использовать для настройки контента вкладки.</span><span class="sxs-lookup"><span data-stu-id="851ef-105">Update the properties of the specified [tab](../resources/teamstab.md). This can be used to configure the content of the tab.</span></span>

## <a name="permissions"></a><span data-ttu-id="851ef-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="851ef-106">Permissions</span></span>
<span data-ttu-id="851ef-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="851ef-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="851ef-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="851ef-109">Permission type</span></span>      | <span data-ttu-id="851ef-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="851ef-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="851ef-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="851ef-111">Delegated (work or school account)</span></span> | <span data-ttu-id="851ef-112">TeamsTab. ReadWrite. ALL, Group. ReadWrite. ALL, Directory. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="851ef-112">TeamsTab.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |
|<span data-ttu-id="851ef-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="851ef-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="851ef-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="851ef-114">Not supported.</span></span>    |
|<span data-ttu-id="851ef-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="851ef-115">Application</span></span> | <span data-ttu-id="851ef-116">TeamsTab. ReadWrite. ALL, Group. ReadWrite. ALL, Directory. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="851ef-116">TeamsTab.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

> <span data-ttu-id="851ef-117">**Примечание**. Этот API поддерживает разрешения администратора.</span><span class="sxs-lookup"><span data-stu-id="851ef-117">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="851ef-118">Глобальные администраторы и администраторы службы Microsoft Teams могут получать доступ к командам, в которых они не состоят.</span><span class="sxs-lookup"><span data-stu-id="851ef-118">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="851ef-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="851ef-119">HTTP request</span></span>
```http
PATCH /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="request-headers"></a><span data-ttu-id="851ef-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="851ef-120">Request headers</span></span>
| <span data-ttu-id="851ef-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="851ef-121">Header</span></span>       | <span data-ttu-id="851ef-122">Значение</span><span class="sxs-lookup"><span data-stu-id="851ef-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="851ef-123">Авторизация</span><span class="sxs-lookup"><span data-stu-id="851ef-123">Authorization</span></span>  | <span data-ttu-id="851ef-p103">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="851ef-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="851ef-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="851ef-126">Content-Type</span></span>  | <span data-ttu-id="851ef-127">application/json</span><span class="sxs-lookup"><span data-stu-id="851ef-127">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="851ef-128">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="851ef-128">Request body</span></span>
<span data-ttu-id="851ef-129">В тексте запроса добавьте представление объекта [Tab](../resources/teamstab.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="851ef-129">In the request body, supply a JSON representation of [tab](../resources/teamstab.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="851ef-130">Отклик</span><span class="sxs-lookup"><span data-stu-id="851ef-130">Response</span></span>

<span data-ttu-id="851ef-131">В случае успешного выполнения этот метод возвращает код отклика `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="851ef-131">If successful, this method returns a `200 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="851ef-132">Пример</span><span class="sxs-lookup"><span data-stu-id="851ef-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="851ef-133">Запрос</span><span class="sxs-lookup"><span data-stu-id="851ef-133">Request</span></span>
<span data-ttu-id="851ef-134">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="851ef-134">The following is an example of the request.</span></span>
```http
PATCH https://graph.microsoft.com/v1.0/teams/{id}/channels/{id}/tabs/{id}
Content-type: application/json
Content-length: 211

{
  "displayName": "My Contoso Tab - updated"
}
```
#### <a name="response"></a><span data-ttu-id="851ef-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="851ef-135">Response</span></span>
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "tabId",
  "displayName": "My Contoso Tab - updated",
  "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('06805b9e-77e3-4b93-ac81-525eb87513b8')",
  "configuration": {
    "entityId": "2DCA2E6C7A10415CAF6B8AB6661B3154",
    "contentUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154/tabView",
    "websiteUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154",
    "removeUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154/uninstallTab"
  },
  "sortOrderIndex": "20",
  "webUrl": "https://teams.microsoft.com/l/channel/19%3ac2e36757ee744c569e70b385e6dd79b6%40thread.skype/tab%3a%3afd736d46-51ed-4c0b-9b23-e67ca354bb24?label=my%20%contoso%to%tab"
}
```

## <a name="see-also"></a><span data-ttu-id="851ef-136">См. также</span><span class="sxs-lookup"><span data-stu-id="851ef-136">See also</span></span>

[<span data-ttu-id="851ef-137">Настройка встроенных типов вкладок</span><span class="sxs-lookup"><span data-stu-id="851ef-137">Configuring the built-in tab types</span></span>](/graph/teams-configuring-builtin-tabs)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Update tab in channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}
-->

