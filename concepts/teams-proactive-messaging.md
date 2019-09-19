---
title: Упреждающий обмен сообщениями с помощью Bot в Microsoft Teams
description: Перед отправкой упреждающего сообщения пользователю Microsoft Teams с помощью настраиваемого приложения сначала необходимо установить Bot с помощью Microsoft Graph.
author: clearab
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: a1cdd206d7cc6db97340ec41727ce9ea64c86510
ms.sourcegitcommit: d8a58221ed1f2b7b7073fd621da4737e11ba53c5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/11/2019
ms.locfileid: "36839201"
---
# <a name="proactive-messaging-using-a-bot-in-microsoft-teams"></a><span data-ttu-id="c1681-103">Упреждающий обмен сообщениями с помощью Bot в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c1681-103">Proactive messaging using a bot in Microsoft Teams</span></span>

<span data-ttu-id="c1681-104">Упреждающее сообщение — это сообщение, отправляемое пользователю Microsoft Teams без инициации беседы пользователем.</span><span class="sxs-lookup"><span data-stu-id="c1681-104">A proactive message is a message sent to a Microsoft Teams user without a user initiating the conversation.</span></span> <span data-ttu-id="c1681-105">Пользовательские приложения в Microsoft Teams могут отправлять активные сообщения пользователям с помощью программы Bot.</span><span class="sxs-lookup"><span data-stu-id="c1681-105">Custom apps in Microsoft Teams can send proactive messages to users using a bot.</span></span> <span data-ttu-id="c1681-106">Тем не менее, для этого необходимо установить робот в качестве личного приложения или в команду, членом которой является пользователь.</span><span class="sxs-lookup"><span data-stu-id="c1681-106">However, to do so, the bot needs to be installed either as a personal app, or in a team that the user is a member of.</span></span> <span data-ttu-id="c1681-107">Это требование может быть недопустимым в сценариях, в которых необходимо заблаговременно заданное сообщение для группы пользователей, у которых может быть установлено приложение Teams.</span><span class="sxs-lookup"><span data-stu-id="c1681-107">This requirement can be prohibitive in scenarios where you need to proactively message a group of users that might or might not have the Teams app installed.</span></span>

<span data-ttu-id="c1681-108">В этой статье рассказывается, как можно объединить Microsoft Graph с приложением Microsoft Teams, чтобы установить приложение для пользователей, а затем использовать приложение Teams для отправки им упреждающего сообщения без необходимости вручную устанавливать приложение.</span><span class="sxs-lookup"><span data-stu-id="c1681-108">This article outlines how you can combine Microsoft Graph with a Microsoft Teams app to install the app for your users and then use your Teams app to send them a proactive message, without requiring them to manually install the app.</span></span>

<span data-ttu-id="c1681-109">На высоком уровне необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c1681-109">At a high level, you'll need to:</span></span>

* [<span data-ttu-id="c1681-110">Создание приложения Teams и программы Bot</span><span class="sxs-lookup"><span data-stu-id="c1681-110">Create your Teams app and bot</span></span>](#create-your-teams-app-and-bot)
* [<span data-ttu-id="c1681-111">Развертывание приложения в каталоге приложений клиента</span><span class="sxs-lookup"><span data-stu-id="c1681-111">Deploy your app to your tenant app catalog</span></span>](#deploy-your-app-to-your-tenant-app-catalog)
* [<span data-ttu-id="c1681-112">Установка приложения для пользователей</span><span class="sxs-lookup"><span data-stu-id="c1681-112">Install the app for your users</span></span>](#install-the-app-for-your-users)

## <a name="create-your-teams-app-and-bot"></a><span data-ttu-id="c1681-113">Создание приложения Teams и программы Bot</span><span class="sxs-lookup"><span data-stu-id="c1681-113">Create your Teams app and bot</span></span>

<span data-ttu-id="c1681-114">Если у вас еще нет приложения Microsoft Teams с роботом, который может отправить сообщение, необходимо создать его.</span><span class="sxs-lookup"><span data-stu-id="c1681-114">If you do not already have a Microsoft Teams app with a bot that can send the message, you'll need to create one.</span></span> <span data-ttu-id="c1681-115">В документации по платформе Teams вы можете ознакомиться с разделом [Add Боты to Apps to Teams](https://docs.microsoft.com/microsoftteams/platform/concepts/bots/bots-overview) .</span><span class="sxs-lookup"><span data-stu-id="c1681-115">See [Add bots to Teams apps](https://docs.microsoft.com/microsoftteams/platform/concepts/bots/bots-overview) in the Teams platform documentation.</span></span> <span data-ttu-id="c1681-116">Сведения о создании почтового робота для упреждающего обмена сообщениями можно узнать в статье [профилактической системы обмена сообщениями для Боты](https://docs.microsoft.com/microsoftteams/platform/concepts/bots/bot-conversations/bots-conv-proactive).</span><span class="sxs-lookup"><span data-stu-id="c1681-116">For specifics about creating a bot for proactive messaging, see [Proactive messaging for bots](https://docs.microsoft.com/microsoftteams/platform/concepts/bots/bot-conversations/bots-conv-proactive).</span></span>

<span data-ttu-id="c1681-117">Вы также можете использовать [шаблон приложения Communicator компании](https://github.com/OfficeDev/microsoft-teams-company-communicator-app) в качестве хорошей отправной точки для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="c1681-117">You can also use the [Company Communicator app template](https://github.com/OfficeDev/microsoft-teams-company-communicator-app) as a good starting point for your app.</span></span> <span data-ttu-id="c1681-118">Этот шаблон приложения — это готовое приложение Microsoft Teams, которое может создавать, планировать и распространять сообщения всей компании.</span><span class="sxs-lookup"><span data-stu-id="c1681-118">This app template is a production-ready Microsoft Teams app capable of creating, scheduling, and distributing company-wide messages.</span></span>

<span data-ttu-id="c1681-119">При создании приложения убедитесь, что вы захотите заметку о том `id` , что вы используете в манифесте приложения; Вам потребуется установить приложение на следующем этапе.</span><span class="sxs-lookup"><span data-stu-id="c1681-119">When creating your app, make sure that you take note of the `id` you use in your application manifest; you'll need it to install the app in a subsequent step.</span></span>

<span data-ttu-id="c1681-120">Если вы делаете это для большой организации, приветственные сообщения от ленты смогут регулироваться.</span><span class="sxs-lookup"><span data-stu-id="c1681-120">If you're doing this for a large organization, the welcome messages from your bot might get throttled.</span></span> <span data-ttu-id="c1681-121">Если это возможно, выполните установку в пакетах и реализуйте функции обратной передачи в интерфейсе Bot.</span><span class="sxs-lookup"><span data-stu-id="c1681-121">If possible, perform the installations in batches, and implement back-off functionality in your bot.</span></span> <span data-ttu-id="c1681-122">Подробнее: [ограничение скорости обработки](/microsoftteams/platform/concepts/bots/rate-limit).</span><span class="sxs-lookup"><span data-stu-id="c1681-122">For details, see [handling rate limiting](/microsoftteams/platform/concepts/bots/rate-limit).</span></span>

## <a name="deploy-your-app-to-your-tenant-app-catalog"></a><span data-ttu-id="c1681-123">Развертывание приложения в каталоге приложений клиента</span><span class="sxs-lookup"><span data-stu-id="c1681-123">Deploy your app to your tenant app catalog</span></span>

<span data-ttu-id="c1681-124">Microsoft Graph может устанавливать только приложения, добавленные в каталог приложений клиента, или доступные в общедоступном магазине приложений Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c1681-124">Microsoft Graph can only install apps that have been added to your tenant app catalog, or are available in the public Microsoft Teams app store.</span></span> <span data-ttu-id="c1681-125">При работе с новым приложением необходимо убедиться в том, что он является [каталогом приложений клиента](https://docs.microsoft.com/microsoftteams/platform/publishing/apps-publish#microsoft-teams-tenant-app-catalog).</span><span class="sxs-lookup"><span data-stu-id="c1681-125">If you're working with a new app, you'll need to make sure it is [tenant app catalog](https://docs.microsoft.com/microsoftteams/platform/publishing/apps-publish#microsoft-teams-tenant-app-catalog).</span></span>

## <a name="install-the-app-for-your-users"></a><span data-ttu-id="c1681-126">Установка приложения для пользователей</span><span class="sxs-lookup"><span data-stu-id="c1681-126">Install the app for your users</span></span>

<span data-ttu-id="c1681-127">Чтобы установить приложение Teams для пользователей, сначала необходимо убедиться, что приложение Microsoft Graph имеет необходимые разрешения — вам потребуется User. ReadWrite. ALL или Directory. ReadWrite. ALL, чтобы установить приложение Teams.</span><span class="sxs-lookup"><span data-stu-id="c1681-127">To install the Teams app for your users, you'll first need to ensure that your Microsoft Graph application has the right permissions – you'll need User.ReadWrite.All or Directory.ReadWrite.All to install the Teams app.</span></span> <span data-ttu-id="c1681-128">Кроме того, вам потребуется чат. Read. ALL для последующего этапа.</span><span class="sxs-lookup"><span data-stu-id="c1681-128">You'll also need Chat.Read.All for a subsequent step.</span></span> <span data-ttu-id="c1681-129">Для обоих разрешений требуется согласие администратора, и вам потребуется использовать разрешения приложения, а не делегирования пользователя, так как вы будете устанавливать приложения для пользователей, отличных от самого себя.</span><span class="sxs-lookup"><span data-stu-id="c1681-129">Both permissions will require admin consent, and you'll need to use application permissions rather than user delegated because you will be installing apps to users other than yourself.</span></span>

### <a name="check-to-see-if-the-app-is-already-installed"></a><span data-ttu-id="c1681-130">Проверка того, установлено ли приложение</span><span class="sxs-lookup"><span data-stu-id="c1681-130">Check to see if the app is already installed</span></span>

<span data-ttu-id="c1681-131">Сначала необходимо проверить, установлено ли приложение Teams для тех пользователей, которые вы хотите установить, как показано в примере.</span><span class="sxs-lookup"><span data-stu-id="c1681-131">First, you'll want to check to see if your Teams app is already installed for the users you want to install it from, as shown in the example.</span></span>

```http
GET /users/{user-id}/teamwork/installedApps?$expand=teamsAppDefinition&$filter=teamsAppDefinition/teamsAppId eq '{teamsAppid}'
```

<span data-ttu-id="c1681-132">Где `{teamsAppId}` — `id` это манифест приложения Teams, который вы внесли ранее.</span><span class="sxs-lookup"><span data-stu-id="c1681-132">Where `{teamsAppId}` is the `id` in the Teams app manifest that you made note of previously.</span></span> <span data-ttu-id="c1681-133">Обратите внимание, что это может отличаться `appid` от вызовов Microsoft Graph, а также от `botId`.</span><span class="sxs-lookup"><span data-stu-id="c1681-133">Note that this might be different from your `appid` for Microsoft Graph calls, and from your `botId`.</span></span> <span data-ttu-id="c1681-134">Может потребоваться вручную установить приложение для пользователя и протестировать вызов для этого пользователя, чтобы убедиться, что вы получили правильное `id` значение.</span><span class="sxs-lookup"><span data-stu-id="c1681-134">You might find it useful to manually install the app for a user and test the call against that user to ensure that you've got the correct `id` value.</span></span>

<span data-ttu-id="c1681-135">Вызов возвратит пустой массив, если приложение не установлено, или массив с одним [теамсаппинсталлатион](/graph/api/resources/teamsappinstallation?view=graph-rest-beta) , если он уже установлен.</span><span class="sxs-lookup"><span data-stu-id="c1681-135">The call will return an empty array if the app is not installed, or an array with a single [teamsAppInstallation](/graph/api/resources/teamsappinstallation?view=graph-rest-beta) if it is already installed.</span></span>

### <a name="install-the-app"></a><span data-ttu-id="c1681-136">Установка приложения</span><span class="sxs-lookup"><span data-stu-id="c1681-136">Install the app</span></span>

<span data-ttu-id="c1681-137">Если приложение еще не установлено для этого пользователя, его можно установить, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="c1681-137">If the app is not already installed for that user, you can then install it as shown in the following example.</span></span>

```http
POST /users/{user-id}/teamwork/installedApps
{
   "teamsApp@odata.bind" : "https://graph.microsoft.com/beta/appCatalogs/teamsApps/{teamsAppid}"
}
```

<span data-ttu-id="c1681-138">Для получения дополнительных сведений обратитесь [к разделу Установка приложения для пользователя](/graph/api/user-add-teamsappinstallation?view=graph-rest-beta).</span><span class="sxs-lookup"><span data-stu-id="c1681-138">For more information, see [Install app for user](/graph/api/user-add-teamsappinstallation?view=graph-rest-beta).</span></span>

<span data-ttu-id="c1681-139">Если у пользователя есть запущенные Microsoft Teams, то, возможно, они не увидят установки приложения, поэтому для его установки может потребоваться перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="c1681-139">If the user has Microsoft Teams running, they might or might not see the app installation right away – they might need to restart the app to see the installation.</span></span>

## <a name="get-the-chat-thread-id"></a><span data-ttu-id="c1681-140">Получение идентификатора потока чата</span><span class="sxs-lookup"><span data-stu-id="c1681-140">Get the chat thread ID</span></span>

<span data-ttu-id="c1681-141">Когда приложение устанавливается для пользователя, робот получит `conversationUpdate` событие, которое будет содержать необходимые сведения для отправки упреждающего сообщения.</span><span class="sxs-lookup"><span data-stu-id="c1681-141">When the app is installed for the user, the bot will get receive a `conversationUpdate` event that will contain the necessary information for it to send the proactive message.</span></span> <span data-ttu-id="c1681-142">Дополнительные сведения: [события Bot](https://docs.microsoft.com/microsoftteams/platform/concepts/bots/bots-notifications).</span><span class="sxs-lookup"><span data-stu-id="c1681-142">For more information, see [Bot events](https://docs.microsoft.com/microsoftteams/platform/concepts/bots/bots-notifications).</span></span>

<span data-ttu-id="c1681-143">Если вы потеряли его `chatThreadId`, вы сможете снова найти его, вызвав:</span><span class="sxs-lookup"><span data-stu-id="c1681-143">If you lose the `chatThreadId`, you can find it again by calling:</span></span>

```http
GET /users/{user-id}/chats?$filter=installedApps/any(a:a/teamsApp/id eq '{teamsAppid}'
```

<span data-ttu-id="c1681-144">Свойство **ID** результата — идентификатор chatThread.</span><span class="sxs-lookup"><span data-stu-id="c1681-144">The **id** property of the result is the chatThread ID.</span></span>

## <a name="sending-the-message"></a><span data-ttu-id="c1681-145">Отправка сообщения</span><span class="sxs-lookup"><span data-stu-id="c1681-145">Sending the message</span></span>

<span data-ttu-id="c1681-146">Теперь, когда у ленты есть необходимые сведения, вы можете [Отправить упреждающее сообщение](https://docs.microsoft.com/microsoftteams/platform/concepts/bots/bot-conversations/bots-conv-proactive).</span><span class="sxs-lookup"><span data-stu-id="c1681-146">Now that your bot has the necessary information, you can [send a proactive message](https://docs.microsoft.com/microsoftteams/platform/concepts/bots/bot-conversations/bots-conv-proactive).</span></span>

## <a name="c-sample"></a><span data-ttu-id="c1681-147">Пример кода на языке C#</span><span class="sxs-lookup"><span data-stu-id="c1681-147">C# sample</span></span>

<span data-ttu-id="c1681-148">В https://github.com/microsoftgraph/contoso-airlines-teams-sample/tree/nkramer-promsg разделе (Обратите внимание на ветвь).</span><span class="sxs-lookup"><span data-stu-id="c1681-148">See https://github.com/microsoftgraph/contoso-airlines-teams-sample/tree/nkramer-promsg (note the branch).</span></span>
<span data-ttu-id="c1681-149">Интересный код находится `InstallAppToAllUsers()` в [GraphService.CS](https://github.com/microsoftgraph/contoso-airlines-teams-sample/blob/nkramer-promsg/project/Models/GraphService.cs).</span><span class="sxs-lookup"><span data-stu-id="c1681-149">Interesting code is in `InstallAppToAllUsers()` in [GraphService.cs](https://github.com/microsoftgraph/contoso-airlines-teams-sample/blob/nkramer-promsg/project/Models/GraphService.cs).</span></span>