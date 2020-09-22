---
title: Создание команды
description: Создание новой команды.
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: a1cbf92ad651e87f68ef10f2e113af3273427560
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47978477"
---
# <a name="create-team"></a><span data-ttu-id="c6eb6-103">Создание команды</span><span class="sxs-lookup"><span data-stu-id="c6eb6-103">Create team</span></span>

<span data-ttu-id="c6eb6-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="c6eb6-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="c6eb6-105">Создание новой [команды](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="c6eb6-105">Create a new [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="c6eb6-106">Разрешения</span><span class="sxs-lookup"><span data-stu-id="c6eb6-106">Permissions</span></span>

<span data-ttu-id="c6eb6-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c6eb6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="c6eb6-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="c6eb6-109">Permission type</span></span>                        | <span data-ttu-id="c6eb6-110">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="c6eb6-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="c6eb6-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c6eb6-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="c6eb6-112">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c6eb6-112">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |
| <span data-ttu-id="c6eb6-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="c6eb6-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c6eb6-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-114">Not supported.</span></span>                              |
| <span data-ttu-id="c6eb6-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="c6eb6-115">Application</span></span>                            | <span data-ttu-id="c6eb6-116">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c6eb6-116">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c6eb6-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="c6eb6-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /teams
```

## <a name="request-headers"></a><span data-ttu-id="c6eb6-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="c6eb6-118">Request headers</span></span>

| <span data-ttu-id="c6eb6-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c6eb6-119">Header</span></span>        | <span data-ttu-id="c6eb6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c6eb6-120">Value</span></span>                     |
| :------------ | :------------------------ |
| <span data-ttu-id="c6eb6-121">Авторизация</span><span class="sxs-lookup"><span data-stu-id="c6eb6-121">Authorization</span></span> | <span data-ttu-id="c6eb6-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c6eb6-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c6eb6-124">Content-Type</span></span>  | <span data-ttu-id="c6eb6-125">application/json</span><span class="sxs-lookup"><span data-stu-id="c6eb6-125">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="c6eb6-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="c6eb6-126">Request body</span></span>

<span data-ttu-id="c6eb6-127">Предоставьте в тексте запроса описание объекта [team](../resources/team.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-127">In the request body, supply a JSON representation of a [team](../resources/team.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="c6eb6-128">Отклик</span><span class="sxs-lookup"><span data-stu-id="c6eb6-128">Response</span></span>

<span data-ttu-id="c6eb6-129">В случае успешного выполнения этот API возвращает отклик `202 Accepted`, содержащий ссылку на [teamsAsyncOperation](../resources/teamsasyncoperation.md).</span><span class="sxs-lookup"><span data-stu-id="c6eb6-129">If successful, this API returns a `202 Accepted` response containing a link to the [teamsAsyncOperation](../resources/teamsasyncoperation.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c6eb6-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="c6eb6-130">Examples</span></span>

### <a name="example-1-delegated-permissions"></a><span data-ttu-id="c6eb6-131">Пример 1. Делегированные разрешения</span><span class="sxs-lookup"><span data-stu-id="c6eb6-131">Example 1: Delegated permissions</span></span>

<span data-ttu-id="c6eb6-132">Ниже приведен пример минимального запроса.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-132">The following is an example of a minimal request.</span></span> <span data-ttu-id="c6eb6-133">Исключив другие свойства, клиент неявно принимает значения по умолчанию из готового шаблона, представленного объектом `template`.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-133">By omitting other properties, the client is implicitly taking defaults from the pre-defined template represented by `template`.</span></span>

#### <a name="request"></a><span data-ttu-id="c6eb6-134">Запрос</span><span class="sxs-lookup"><span data-stu-id="c6eb6-134">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_team_post"
}-->
```http
POST https://graph.microsoft.com/v1.0/teams
Content-Type: application/json

{
  "template@odata.bind": "https://graph.microsoft.com/v1.0/teamsTemplates('standard')",
  "displayName": "My Sample Team",
  "description": "My Sample Team’s Description"
}
```

##### <a name="response"></a><span data-ttu-id="c6eb6-135">Отклик</span><span class="sxs-lookup"><span data-stu-id="c6eb6-135">Response</span></span>
<!-- {
  "blockType": "response",
  "name": "create_team_post",
  "@odata.type": "microsoft.graph.team"
}-->
```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
Content-Length: 0
```

### <a name="example-2-application-permissions"></a><span data-ttu-id="c6eb6-136">Пример 2. Разрешения для приложения</span><span class="sxs-lookup"><span data-stu-id="c6eb6-136">Example 2: Application permissions</span></span>

<span data-ttu-id="c6eb6-137">Ниже приведен пример минимального запроса с использованием разрешений для приложения.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-137">The following is an example of a minimal request using application permissions.</span></span> <span data-ttu-id="c6eb6-138">Исключив другие свойства, клиент неявно принимает значения по умолчанию из готового шаблона, представленного объектом `template`.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-138">By omitting other properties, the client is implicitly taking defaults from the predefined template represented by `template`.</span></span> <span data-ttu-id="c6eb6-139">При отправке запроса с разрешениями для приложения ресурс [user](../resources/user.md) должен быть указан в коллекции `owners`.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-139">When issuing a request with application permissions, a [user](../resources/user.md) must be specified in the `owners` collection.</span></span>

#### <a name="request"></a><span data-ttu-id="c6eb6-140">Запрос</span><span class="sxs-lookup"><span data-stu-id="c6eb6-140">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_team_post_minimal"
}-->
```http
POST https://graph.microsoft.com/v1.0/teams
Content-Type: application/json

{
  "template@odata.bind": "https://graph.microsoft.com/v1.0/teamsTemplates('standard')",
  "displayName": "My Sample Team",
  "description": "My Sample Team’s Description",
  "owners@odata.bind": [
    "https://graph.microsoft.com/v1.0/users('userId')"
  ]
}
```


#### <a name="response"></a><span data-ttu-id="c6eb6-141">Отклик</span><span class="sxs-lookup"><span data-stu-id="c6eb6-141">Response</span></span>
<!-- {
  "blockType": "response",
  "name": "create_team_post_minimal",
  "@odata.type": "microsoft.graph.team"
}-->
```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
Content-Length: 0
```

### <a name="example-3-create-a-team-with-multiple-channels-installed-apps-and-pinned-tabs-using-delegated-permissions"></a><span data-ttu-id="c6eb6-142">Пример 3. Создание команды с несколькими каналами, установленными приложениями и закрепленными вкладками с использованием делегированных разрешений</span><span class="sxs-lookup"><span data-stu-id="c6eb6-142">Example 3: Create a team with multiple channels, installed apps, and pinned tabs using delegated permissions</span></span>

<span data-ttu-id="c6eb6-143">Ниже приведен запрос с указанием полного набора полезных данных.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-143">The following is a request with a full payload.</span></span> <span data-ttu-id="c6eb6-144">Клиент может переопределить значения в базовом шаблоне и добавить элементы со значениями массива в пределах, допускаемых правилами проверки для объекта `specialization`.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-144">The client can override values in the base template and add to array-valued items to the extent allowed by validation rules for the `specialization`.</span></span>

#### <a name="request"></a><span data-ttu-id="c6eb6-145">Запрос</span><span class="sxs-lookup"><span data-stu-id="c6eb6-145">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_team_post_full_payload"
}-->
```http
POST https://graph.microsoft.com/v1.0/teams
Content-Type: application/json

{
    "template@odata.bind": "https://graph.microsoft.com/v1.0/teamsTemplates('standard')",
    "visibility": "Private",
    "displayName": "Sample Engineering Team",
    "description": "This is a sample engineering team, used to showcase the range of properties supported by this API",
    "channels": [
        {
            "displayName": "Announcements 📢",
            "isFavoriteByDefault": true,
            "description": "This is a sample announcements channel that is favorited by default. Use this channel to make important team, product, and service announcements."
        },
        {
            "displayName": "Training 🏋️",
            "isFavoriteByDefault": true,
            "description": "This is a sample training channel, that is favorited by default, and contains an example of pinned website and YouTube tabs.",
            "tabs": [
                {
                    "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.web')",
                    "name": "A Pinned Website",
                    "configuration": {
                        "contentUrl": "https://docs.microsoft.com/microsoftteams/microsoft-teams"
                    }
                },
                {
                    "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.youtube')",
                    "name": "A Pinned YouTube Video",
                    "configuration": {
                        "contentUrl": "https://tabs.teams.microsoft.com/Youtube/Home/YoutubeTab?videoId=X8krAMdGvCQ",
                        "websiteUrl": "https://www.youtube.com/watch?v=X8krAMdGvCQ"
                    }
                }
            ]
        },
        {
            "displayName": "Planning 📅 ",
            "description": "This is a sample of a channel that is not favorited by default, these channels will appear in the more channels overflow menu.",
            "isFavoriteByDefault": false
        },
        {
            "displayName": "Issues and Feedback 🐞",
            "description": "This is a sample of a channel that is not favorited by default, these channels will appear in the more channels overflow menu."
        }
    ],
    "memberSettings": {
        "allowCreateUpdateChannels": true,
        "allowDeleteChannels": true,
        "allowAddRemoveApps": true,
        "allowCreateUpdateRemoveTabs": true,
        "allowCreateUpdateRemoveConnectors": true
    },
    "guestSettings": {
        "allowCreateUpdateChannels": false,
        "allowDeleteChannels": false
    },
    "funSettings": {
        "allowGiphy": true,
        "giphyContentRating": "Moderate",
        "allowStickersAndMemes": true,
        "allowCustomMemes": true
    },
    "messagingSettings": {
        "allowUserEditMessages": true,
        "allowUserDeleteMessages": true,
        "allowOwnerDeleteMessages": true,
        "allowTeamMentions": true,
        "allowChannelMentions": true
    },
    "discoverySettings": {
        "showInTeamsSearchAndSuggestions": true
    },
    "installedApps": [
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.vsts')"
        },
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('1542629c-01b3-4a6d-8f76-1938b779e48d')"
        }
    ]
}
```


#### <a name="response"></a><span data-ttu-id="c6eb6-146">Отклик</span><span class="sxs-lookup"><span data-stu-id="c6eb6-146">Response</span></span>
<!-- {
  "blockType": "response",
  "name": "create_team_post_full_payload",
  "@odata.type": "microsoft.graph.team"
}-->
```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
Content-Length: 0
```

### <a name="example-4-create-a-team-from-group"></a><span data-ttu-id="c6eb6-147">Пример 4. Создание команды из группы</span><span class="sxs-lookup"><span data-stu-id="c6eb6-147">Example 4: Create a team from group</span></span>

<span data-ttu-id="c6eb6-148">В следующем примере показано, как можно создать новую [команду](../resources/team.md) из [группы](../resources/group.md) с учетом **groupId**.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-148">The following example shows how you can create a new [team](../resources/team.md) from a [group](../resources/group.md), given a **groupId**.</span></span>

<span data-ttu-id="c6eb6-149">Обратите внимание на некоторые моменты, связанные с этим вызовом:</span><span class="sxs-lookup"><span data-stu-id="c6eb6-149">A few thing to note about this call:</span></span>

* <span data-ttu-id="c6eb6-150">Чтобы создать команду, в группе, из которой она создается, должен быть хотя бы один владелец.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-150">In order to create a team, the group you're creating it from must have a least one owner.</span></span>
* <span data-ttu-id="c6eb6-151">Созданная команда всегда наследует из группы отображаемое имя, параметры видимости, специализацию и владельцев.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-151">The team that's created will always inherit from the group's display name, visibility, specialization, and owners.</span></span> <span data-ttu-id="c6eb6-152">Поэтому, когда выполняется этот вызов с использованием свойства **group@odata.bind**, включение свойств **displayName**, **visibility**, **specialization** или **owners@odata.bind** команды возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-152">Therefore, when making this call with the **group@odata.bind** property, the inclusion of team **displayName**, **visibility**, **specialization**, or **owners@odata.bind** properties will return an error.</span></span>
* <span data-ttu-id="c6eb6-153">Если группа создана менее 15 минут назад, вызов метода "Создание команды" может завершиться ошибкой с кодом 404 из-за задержек репликации.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-153">If the group was created less than 15 minutes ago, it's possible for the Create team call to fail with a 404 error code due to replication delays.</span></span> <span data-ttu-id="c6eb6-154">Рекомендуется повторить вызов метода "Создание команды" три раза с 10-секундной задержкой между вызовами.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-154">We recommend that you retry the Create team call three times, with a 10 second delay between calls.</span></span>


#### <a name="request"></a><span data-ttu-id="c6eb6-155">Запрос</span><span class="sxs-lookup"><span data-stu-id="c6eb6-155">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_team_from_group"
}-->
```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json

{
  "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates('standard')",
  "group@odata.bind": "https://graph.microsoft.com/v1.0/groups('groupId')"
}
```


#### <a name="response"></a><span data-ttu-id="c6eb6-156">Отклик</span><span class="sxs-lookup"><span data-stu-id="c6eb6-156">Response</span></span>
<!-- {
  "blockType": "response",
  "name": "create_team_from_group",
  "@odata.type": "microsoft.graph.team"
}-->
```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
Content-Length: 0
```

### <a name="example-5-create-a-team-from-a-group-with-multiple-channels-installed-apps-and-pinned-tabs"></a><span data-ttu-id="c6eb6-157">Пример 5. Создание команды из группы с несколькими каналами, установленными приложениями и закрепленными вкладками</span><span class="sxs-lookup"><span data-stu-id="c6eb6-157">Example 5: Create a team from a group with multiple channels, installed apps, and pinned tabs</span></span>

<span data-ttu-id="c6eb6-158">Ниже указан запрос, преобразующий существующую группу с расширенными свойствами, в результате чего создается команда с несколькими каналами, установленными приложениями и закрепленными вкладками.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-158">The following is a request that converts an existing group with extended properties which will create the team with multiple channels, installed apps, and pinned tabs.</span></span>

<span data-ttu-id="c6eb6-159">Дополнительные сведения о поддерживаемых базовых типах шаблонов и свойствах см. в статье [Начало работы с шаблонами Teams](/MicrosoftTeams/get-started-with-teams-templates).</span><span class="sxs-lookup"><span data-stu-id="c6eb6-159">To learn more about supported base template types and supported properties, see [Get started with Teams templates](/MicrosoftTeams/get-started-with-teams-templates).</span></span>

#### <a name="request"></a><span data-ttu-id="c6eb6-160">Запрос</span><span class="sxs-lookup"><span data-stu-id="c6eb6-160">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "convert_team_from_group"
}-->
```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json

{
  "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates('standard')",
  "group@odata.bind": "https://graph.microsoft.com/v1.0/groups('groupId')",
  "channels": [
        {
            "displayName": "Class Announcements 📢",
            "isFavoriteByDefault": true
        },
        {
            "displayName": "Homework 🏋️",
            "isFavoriteByDefault": true,
        }
    ],
    "memberSettings": {
        "allowCreateUpdateChannels": false,
        "allowDeleteChannels": false,
        "allowAddRemoveApps": false,
        "allowCreateUpdateRemoveTabs": false,
        "allowCreateUpdateRemoveConnectors": false
    },
    "installedApps": [
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.vsts')"
        },
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('1542629c-01b3-4a6d-8f76-1938b779e48d')"
        }
    ]
}
```


#### <a name="response"></a><span data-ttu-id="c6eb6-161">Отклик</span><span class="sxs-lookup"><span data-stu-id="c6eb6-161">Response</span></span>
<!-- {
  "blockType": "response",
  "name": "convert_team_from_group",
  "@odata.type": "microsoft.graph.team"
}-->
```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
Content-Length: 0
```

### <a name="example-6-create-a-team-with-a-non-standard-base-template-type"></a><span data-ttu-id="c6eb6-162">Пример 6. Создание команды с использованием нестандартного базового типа шаблона</span><span class="sxs-lookup"><span data-stu-id="c6eb6-162">Example 6: Create a team with a non-standard base template type</span></span>

<span data-ttu-id="c6eb6-163">Базовые типы шаблонов — это специальные шаблоны, созданные корпорацией Майкрософт для определенных отраслей.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-163">Base template types are special templates that Microsoft created for specific industries.</span></span> <span data-ttu-id="c6eb6-164">Эти базовые шаблоны зачастую содержат защищаемые приложения, недоступные в свойствах хранилища и команды, которые еще не поддерживаются по отдельности в шаблонах Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-164">These base templates often contain proprietary apps that aren't available in the store and team properties that are not yet supported individually in Microsoft Teams templates.</span></span>

<span data-ttu-id="c6eb6-165">Чтобы создать команду на основе нестандартного базового шаблона, потребуется изменить значение свойства `template@odata.bind` со `standard` на название этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-165">To create a team from a non-standard base template, you’ll want to change the `template@odata.bind` property in the request body from `standard` to point to the specific base template you’d like to create.</span></span>

<span data-ttu-id="c6eb6-166">Дополнительные сведения о поддерживаемых базовых типах шаблонов см. в статье [Начало работы с шаблонами Teams](/MicrosoftTeams/get-started-with-teams-templates).</span><span class="sxs-lookup"><span data-stu-id="c6eb6-166">To learn more about supported base template types, see [Get started with Teams templates](/MicrosoftTeams/get-started-with-teams-templates).</span></span>

#### <a name="request"></a><span data-ttu-id="c6eb6-167">Запрос</span><span class="sxs-lookup"><span data-stu-id="c6eb6-167">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "convert_team_from_non_standard"
}-->
```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json

{
  "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates('educationClass')",
  "displayName": "My Class Team",
  "description": "My Class Team’s Description"
}
```

#### <a name="response"></a><span data-ttu-id="c6eb6-168">Отклик</span><span class="sxs-lookup"><span data-stu-id="c6eb6-168">Response</span></span>
<!-- {
  "blockType": "response",
  "name": "convert_team_from_non_standard",
  "@odata.type": "microsoft.graph.team"
}-->
```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
Content-Length: 0
```

### <a name="example-7-create-a-team-with-a-non-standard-base-template-type-with-extended-properties"></a><span data-ttu-id="c6eb6-169">Пример 7. Создание команды с использованием нестандартного базового типа шаблона с расширенными свойствами</span><span class="sxs-lookup"><span data-stu-id="c6eb6-169">Example 7: Create a team with a non-standard base template type with extended properties</span></span>

<span data-ttu-id="c6eb6-170">Базовые типы шаблонов могут быть расширены с помощью дополнительных свойств. Это позволяет дополнить существующий базовый шаблон дополнительными каналами, приложениями, вкладками и параметрами команды.</span><span class="sxs-lookup"><span data-stu-id="c6eb6-170">Base template types can be extended with additional properties, enabling you to build on an existing base template with additional team settings, channels, apps, or tabs.</span></span>

<span data-ttu-id="c6eb6-171">Дополнительные сведения о поддерживаемых базовых типах шаблонов и свойствах см. в статье [Начало работы с шаблонами Teams](/MicrosoftTeams/get-started-with-teams-templates).</span><span class="sxs-lookup"><span data-stu-id="c6eb6-171">To learn more about supported base template types and supported properties, see [Get started with Teams templates](/MicrosoftTeams/get-started-with-teams-templates).</span></span>

#### <a name="request"></a><span data-ttu-id="c6eb6-172">Запрос</span><span class="sxs-lookup"><span data-stu-id="c6eb6-172">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "convert_team_from_non_standard2"
}-->
```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json

{
  "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates('educationClass')",
  "displayName": "My Class Team",
  "description": "My Class Team’s Description",
  "channels": [
        {
            "displayName": "Class Announcements 📢",
            "isFavoriteByDefault": true
        },
        {
            "displayName": "Homework 🏋️",
            "isFavoriteByDefault": true,
        }
    ],
    "memberSettings": {
        "allowCreateUpdateChannels": false,
        "allowDeleteChannels": false,
        "allowAddRemoveApps": false,
        "allowCreateUpdateRemoveTabs": false,
        "allowCreateUpdateRemoveConnectors": false
    },
    "installedApps": [
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.vsts')"
        },
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('1542629c-01b3-4a6d-8f76-1938b779e48d')"
        }
    ]
}
```

#### <a name="response"></a><span data-ttu-id="c6eb6-173">Ответ</span><span class="sxs-lookup"><span data-stu-id="c6eb6-173">Response</span></span>
<!-- {
  "blockType": "response",
  "name": "convert_team_from_non_standard2",
  "@odata.type": "microsoft.graph.team"
}-->
```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
Content-Length: 0
```

## <a name="see-also"></a><span data-ttu-id="c6eb6-174">См. также</span><span class="sxs-lookup"><span data-stu-id="c6eb6-174">See also</span></span>

- [<span data-ttu-id="c6eb6-175">Доступные шаблоны</span><span class="sxs-lookup"><span data-stu-id="c6eb6-175">Available templates</span></span>](/MicrosoftTeams/get-started-with-teams-templates)
- [<span data-ttu-id="c6eb6-176">Начало работы с шаблонами команд розничной торговли</span><span class="sxs-lookup"><span data-stu-id="c6eb6-176">Getting started with Retail Teams templates</span></span>](https://docs.microsoft.com/MicrosoftTeams/get-started-with-retail-teams-templates)
- [<span data-ttu-id="c6eb6-177">Начало работы с шаблонами команд здравоохранения</span><span class="sxs-lookup"><span data-stu-id="c6eb6-177">Getting started with Healthcare Teams templates</span></span>](https://docs.microsoft.com/MicrosoftTeams/healthcare/healthcare-templates)
- [<span data-ttu-id="c6eb6-178">Создание группы с командой</span><span class="sxs-lookup"><span data-stu-id="c6eb6-178">Creating a group with a team</span></span>](/graph/teams-create-group-and-team)

