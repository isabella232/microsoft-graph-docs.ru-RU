---
title: Создание win32LobApp
description: Создание нового объекта win32LobApp.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 9814f52587ba4351fd573ff03c0c66d121092e6f
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2019
ms.locfileid: "37172116"
---
# <a name="create-win32lobapp"></a><span data-ttu-id="2e057-103">Создание win32LobApp</span><span class="sxs-lookup"><span data-stu-id="2e057-103">Create win32LobApp</span></span>

> <span data-ttu-id="2e057-104">**Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2e057-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="2e057-105">**Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="2e057-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="2e057-106">Создание нового объекта [win32LobApp](../resources/intune-apps-win32lobapp.md) .</span><span class="sxs-lookup"><span data-stu-id="2e057-106">Create a new [win32LobApp](../resources/intune-apps-win32lobapp.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2e057-107">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="2e057-107">Prerequisites</span></span>
<span data-ttu-id="2e057-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2e057-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2e057-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="2e057-110">Permission type</span></span>|<span data-ttu-id="2e057-111">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="2e057-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2e057-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="2e057-112">Delegated (work or school account)</span></span>|<span data-ttu-id="2e057-113">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2e057-113">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="2e057-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="2e057-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2e057-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2e057-115">Not supported.</span></span>|
|<span data-ttu-id="2e057-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="2e057-116">Application</span></span>|<span data-ttu-id="2e057-117">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2e057-117">DeviceManagementApps.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="2e057-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="2e057-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="2e057-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="2e057-119">Request headers</span></span>
|<span data-ttu-id="2e057-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2e057-120">Header</span></span>|<span data-ttu-id="2e057-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2e057-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2e057-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="2e057-122">Authorization</span></span>|<span data-ttu-id="2e057-123">Bearer &lt;token&gt;. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="2e057-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2e057-124">Accept</span><span class="sxs-lookup"><span data-stu-id="2e057-124">Accept</span></span>|<span data-ttu-id="2e057-125">application/json</span><span class="sxs-lookup"><span data-stu-id="2e057-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2e057-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="2e057-126">Request body</span></span>
<span data-ttu-id="2e057-127">В тексте запроса добавьте представление объекта win32LobApp в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="2e057-127">In the request body, supply a JSON representation for the win32LobApp object.</span></span>

<span data-ttu-id="2e057-128">В следующей таблице приведены свойства, необходимые при создании win32LobApp.</span><span class="sxs-lookup"><span data-stu-id="2e057-128">The following table shows the properties that are required when you create the win32LobApp.</span></span>

|<span data-ttu-id="2e057-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="2e057-129">Property</span></span>|<span data-ttu-id="2e057-130">Тип</span><span class="sxs-lookup"><span data-stu-id="2e057-130">Type</span></span>|<span data-ttu-id="2e057-131">Описание</span><span class="sxs-lookup"><span data-stu-id="2e057-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2e057-132">id</span><span class="sxs-lookup"><span data-stu-id="2e057-132">id</span></span>|<span data-ttu-id="2e057-133">Строка</span><span class="sxs-lookup"><span data-stu-id="2e057-133">String</span></span>|<span data-ttu-id="2e057-134">Ключ объекта.</span><span class="sxs-lookup"><span data-stu-id="2e057-134">Key of the entity.</span></span> <span data-ttu-id="2e057-135">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-135">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-136">displayName</span><span class="sxs-lookup"><span data-stu-id="2e057-136">displayName</span></span>|<span data-ttu-id="2e057-137">Строка</span><span class="sxs-lookup"><span data-stu-id="2e057-137">String</span></span>|<span data-ttu-id="2e057-138">Название приложения, которое предоставил или импортировал администратор.</span><span class="sxs-lookup"><span data-stu-id="2e057-138">The admin provided or imported title of the app.</span></span> <span data-ttu-id="2e057-139">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-139">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-140">description</span><span class="sxs-lookup"><span data-stu-id="2e057-140">description</span></span>|<span data-ttu-id="2e057-141">Строка</span><span class="sxs-lookup"><span data-stu-id="2e057-141">String</span></span>|<span data-ttu-id="2e057-142">Описание приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-142">The description of the app.</span></span> <span data-ttu-id="2e057-143">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-143">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-144">publisher</span><span class="sxs-lookup"><span data-stu-id="2e057-144">publisher</span></span>|<span data-ttu-id="2e057-145">String.</span><span class="sxs-lookup"><span data-stu-id="2e057-145">String</span></span>|<span data-ttu-id="2e057-146">Издатель приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-146">The publisher of the app.</span></span> <span data-ttu-id="2e057-147">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-147">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-148">largeIcon</span><span class="sxs-lookup"><span data-stu-id="2e057-148">largeIcon</span></span>|[<span data-ttu-id="2e057-149">mimeContent</span><span class="sxs-lookup"><span data-stu-id="2e057-149">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="2e057-150">Представляет большой значок, который отображается в сведениях о приложении, используется для отправки значка.</span><span class="sxs-lookup"><span data-stu-id="2e057-150">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="2e057-151">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-151">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2e057-152">createdDateTime</span></span>|<span data-ttu-id="2e057-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2e057-153">DateTimeOffset</span></span>|<span data-ttu-id="2e057-154">Дата и время создания приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-154">The date and time the app was created.</span></span> <span data-ttu-id="2e057-155">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-155">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-156">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2e057-156">lastModifiedDateTime</span></span>|<span data-ttu-id="2e057-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2e057-157">DateTimeOffset</span></span>|<span data-ttu-id="2e057-158">Дата и время последнего изменения приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-158">The date and time the app was last modified.</span></span> <span data-ttu-id="2e057-159">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-159">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-160">isFeatured</span><span class="sxs-lookup"><span data-stu-id="2e057-160">isFeatured</span></span>|<span data-ttu-id="2e057-161">Boolean</span><span class="sxs-lookup"><span data-stu-id="2e057-161">Boolean</span></span>|<span data-ttu-id="2e057-162">Значение, которое показывает, отмечено ли приложение как подобранное администратором. Наследуется от объекта [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-162">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-163">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="2e057-163">privacyInformationUrl</span></span>|<span data-ttu-id="2e057-164">String.</span><span class="sxs-lookup"><span data-stu-id="2e057-164">String</span></span>|<span data-ttu-id="2e057-165">URL-адрес заявления о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="2e057-165">The privacy statement Url.</span></span> <span data-ttu-id="2e057-166">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-166">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-167">informationUrl</span><span class="sxs-lookup"><span data-stu-id="2e057-167">informationUrl</span></span>|<span data-ttu-id="2e057-168">String.</span><span class="sxs-lookup"><span data-stu-id="2e057-168">String</span></span>|<span data-ttu-id="2e057-169">URL-адрес страницы с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="2e057-169">The more information Url.</span></span> <span data-ttu-id="2e057-170">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-170">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-171">owner</span><span class="sxs-lookup"><span data-stu-id="2e057-171">owner</span></span>|<span data-ttu-id="2e057-172">String</span><span class="sxs-lookup"><span data-stu-id="2e057-172">String</span></span>|<span data-ttu-id="2e057-173">Владелец приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-173">The owner of the app.</span></span> <span data-ttu-id="2e057-174">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-174">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-175">developer</span><span class="sxs-lookup"><span data-stu-id="2e057-175">developer</span></span>|<span data-ttu-id="2e057-176">String.</span><span class="sxs-lookup"><span data-stu-id="2e057-176">String</span></span>|<span data-ttu-id="2e057-177">Разработчик приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-177">The developer of the app.</span></span> <span data-ttu-id="2e057-178">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-178">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-179">notes</span><span class="sxs-lookup"><span data-stu-id="2e057-179">notes</span></span>|<span data-ttu-id="2e057-180">String.</span><span class="sxs-lookup"><span data-stu-id="2e057-180">String</span></span>|<span data-ttu-id="2e057-181">Заметки для приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-181">Notes for the app.</span></span> <span data-ttu-id="2e057-182">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-182">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-183">uploadState</span><span class="sxs-lookup"><span data-stu-id="2e057-183">uploadState</span></span>|<span data-ttu-id="2e057-184">Int32</span><span class="sxs-lookup"><span data-stu-id="2e057-184">Int32</span></span>|<span data-ttu-id="2e057-185">Состояние отправки.</span><span class="sxs-lookup"><span data-stu-id="2e057-185">The upload state.</span></span> <span data-ttu-id="2e057-186">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-186">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-187">publishingState</span><span class="sxs-lookup"><span data-stu-id="2e057-187">publishingState</span></span>|[<span data-ttu-id="2e057-188">мобилеапппублишингстате</span><span class="sxs-lookup"><span data-stu-id="2e057-188">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="2e057-189">Состояние публикации для приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-189">The publishing state for the app.</span></span> <span data-ttu-id="2e057-190">Приложение невозможно назначить, если оно не опубликовано.</span><span class="sxs-lookup"><span data-stu-id="2e057-190">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="2e057-191">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-191">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md).</span></span> <span data-ttu-id="2e057-192">Возможные значения: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="2e057-192">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="2e057-193">isAssigned</span><span class="sxs-lookup"><span data-stu-id="2e057-193">isAssigned</span></span>|<span data-ttu-id="2e057-194">Boolean</span><span class="sxs-lookup"><span data-stu-id="2e057-194">Boolean</span></span>|<span data-ttu-id="2e057-195">Значение, указывающее, назначено ли приложение по крайней мере одной группе.</span><span class="sxs-lookup"><span data-stu-id="2e057-195">The value indicating whether the app is assigned to at least one group.</span></span> <span data-ttu-id="2e057-196">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-196">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-197">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="2e057-197">roleScopeTagIds</span></span>|<span data-ttu-id="2e057-198">Коллекция строк</span><span class="sxs-lookup"><span data-stu-id="2e057-198">String collection</span></span>|<span data-ttu-id="2e057-199">Список идентификаторов тегов области для этого мобильного приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-199">List of scope tag ids for this mobile app.</span></span> <span data-ttu-id="2e057-200">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-200">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-201">депендентаппкаунт</span><span class="sxs-lookup"><span data-stu-id="2e057-201">dependentAppCount</span></span>|<span data-ttu-id="2e057-202">Int32</span><span class="sxs-lookup"><span data-stu-id="2e057-202">Int32</span></span>|<span data-ttu-id="2e057-203">Общее количество зависимостей для дочернего приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-203">The total number of dependencies the child app has.</span></span> <span data-ttu-id="2e057-204">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-204">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="2e057-205">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="2e057-205">committedContentVersion</span></span>|<span data-ttu-id="2e057-206">String.</span><span class="sxs-lookup"><span data-stu-id="2e057-206">String</span></span>|<span data-ttu-id="2e057-207">Внутренняя версия подтвержденного содержимого.</span><span class="sxs-lookup"><span data-stu-id="2e057-207">The internal committed content version.</span></span> <span data-ttu-id="2e057-208">Наследуется от [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-208">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2e057-209">fileName</span><span class="sxs-lookup"><span data-stu-id="2e057-209">fileName</span></span>|<span data-ttu-id="2e057-210">String</span><span class="sxs-lookup"><span data-stu-id="2e057-210">String</span></span>|<span data-ttu-id="2e057-211">Имя основного файла бизнес-приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-211">The name of the main Lob application file.</span></span> <span data-ttu-id="2e057-212">Наследуется от [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-212">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2e057-213">size</span><span class="sxs-lookup"><span data-stu-id="2e057-213">size</span></span>|<span data-ttu-id="2e057-214">Int64</span><span class="sxs-lookup"><span data-stu-id="2e057-214">Int64</span></span>|<span data-ttu-id="2e057-215">Общий размер, включая все отправленные файлы.</span><span class="sxs-lookup"><span data-stu-id="2e057-215">The total size, including all uploaded files.</span></span> <span data-ttu-id="2e057-216">Наследуется от [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2e057-216">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2e057-217">инсталлкоммандлине</span><span class="sxs-lookup"><span data-stu-id="2e057-217">installCommandLine</span></span>|<span data-ttu-id="2e057-218">String.</span><span class="sxs-lookup"><span data-stu-id="2e057-218">String</span></span>|<span data-ttu-id="2e057-219">Командная строка для установки приложения</span><span class="sxs-lookup"><span data-stu-id="2e057-219">The command line to install this app</span></span>|
|<span data-ttu-id="2e057-220">унинсталлкоммандлине</span><span class="sxs-lookup"><span data-stu-id="2e057-220">uninstallCommandLine</span></span>|<span data-ttu-id="2e057-221">String.</span><span class="sxs-lookup"><span data-stu-id="2e057-221">String</span></span>|<span data-ttu-id="2e057-222">Командная строка для удаления приложения</span><span class="sxs-lookup"><span data-stu-id="2e057-222">The command line to uninstall this app</span></span>|
|<span data-ttu-id="2e057-223">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="2e057-223">applicableArchitectures</span></span>|[<span data-ttu-id="2e057-224">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="2e057-224">windowsArchitecture</span></span>](../resources/intune-apps-windowsarchitecture.md)|<span data-ttu-id="2e057-225">Архитектура Windows, которая поддерживается этим приложением.</span><span class="sxs-lookup"><span data-stu-id="2e057-225">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="2e057-226">Возможные значения: `none`, `x86`, `x64`, `arm`, `neutral`, `arm64`.</span><span class="sxs-lookup"><span data-stu-id="2e057-226">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`, `arm64`.</span></span>|
|<span data-ttu-id="2e057-227">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2e057-227">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="2e057-228">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2e057-228">windowsMinimumOperatingSystem</span></span>](../resources/intune-apps-windowsminimumoperatingsystem.md)|<span data-ttu-id="2e057-229">Значение, которое представляет минимальную применимую версию операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2e057-229">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="2e057-230">минимумфридискспацеинмб</span><span class="sxs-lookup"><span data-stu-id="2e057-230">minimumFreeDiskSpaceInMB</span></span>|<span data-ttu-id="2e057-231">Int32</span><span class="sxs-lookup"><span data-stu-id="2e057-231">Int32</span></span>|<span data-ttu-id="2e057-232">Минимальное свободное место на диске, необходимое для установки этого приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-232">The value for the minimum free disk space which is required to install this app.</span></span>|
|<span data-ttu-id="2e057-233">минимуммеморинмб</span><span class="sxs-lookup"><span data-stu-id="2e057-233">minimumMemoryInMB</span></span>|<span data-ttu-id="2e057-234">Int32</span><span class="sxs-lookup"><span data-stu-id="2e057-234">Int32</span></span>|<span data-ttu-id="2e057-235">Значение минимальной физической памяти, необходимой для установки этого приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-235">The value for the minimum physical memory which is required to install this app.</span></span>|
|<span data-ttu-id="2e057-236">минимумнумберофпроцессорс</span><span class="sxs-lookup"><span data-stu-id="2e057-236">minimumNumberOfProcessors</span></span>|<span data-ttu-id="2e057-237">Int32</span><span class="sxs-lookup"><span data-stu-id="2e057-237">Int32</span></span>|<span data-ttu-id="2e057-238">Значение минимального числа процессоров, необходимое для установки этого приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-238">The value for the minimum number of processors which is required to install this app.</span></span>|
|<span data-ttu-id="2e057-239">минимумкпуспидинмхз</span><span class="sxs-lookup"><span data-stu-id="2e057-239">minimumCpuSpeedInMHz</span></span>|<span data-ttu-id="2e057-240">Int32</span><span class="sxs-lookup"><span data-stu-id="2e057-240">Int32</span></span>|<span data-ttu-id="2e057-241">Значение минимальной скорости ЦП, необходимое для установки этого приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-241">The value for the minimum CPU speed which is required to install this app.</span></span>|
|<span data-ttu-id="2e057-242">детектионрулес</span><span class="sxs-lookup"><span data-stu-id="2e057-242">detectionRules</span></span>|<span data-ttu-id="2e057-243">Коллекция [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span><span class="sxs-lookup"><span data-stu-id="2e057-243">[win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md) collection</span></span>|<span data-ttu-id="2e057-244">Правила обнаружения для определения бизнес-приложения Win32 (LoB).</span><span class="sxs-lookup"><span data-stu-id="2e057-244">The detection rules to detect Win32 Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="2e057-245">рекуирементрулес</span><span class="sxs-lookup"><span data-stu-id="2e057-245">requirementRules</span></span>|<span data-ttu-id="2e057-246">Коллекция [win32LobAppRequirement](../resources/intune-apps-win32lobapprequirement.md)</span><span class="sxs-lookup"><span data-stu-id="2e057-246">[win32LobAppRequirement](../resources/intune-apps-win32lobapprequirement.md) collection</span></span>|<span data-ttu-id="2e057-247">Правила требований для обнаружения бизнес-приложения Win32.</span><span class="sxs-lookup"><span data-stu-id="2e057-247">The requirement rules to detect Win32 Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="2e057-248">инсталлекспериенце</span><span class="sxs-lookup"><span data-stu-id="2e057-248">installExperience</span></span>|[<span data-ttu-id="2e057-249">win32LobAppInstallExperience</span><span class="sxs-lookup"><span data-stu-id="2e057-249">win32LobAppInstallExperience</span></span>](../resources/intune-apps-win32lobappinstallexperience.md)|<span data-ttu-id="2e057-250">Установка приложения.</span><span class="sxs-lookup"><span data-stu-id="2e057-250">The install experience for this app.</span></span>|
|<span data-ttu-id="2e057-251">ретурнкодес</span><span class="sxs-lookup"><span data-stu-id="2e057-251">returnCodes</span></span>|<span data-ttu-id="2e057-252">Коллекция [win32LobAppReturnCode](../resources/intune-apps-win32lobappreturncode.md)</span><span class="sxs-lookup"><span data-stu-id="2e057-252">[win32LobAppReturnCode](../resources/intune-apps-win32lobappreturncode.md) collection</span></span>|<span data-ttu-id="2e057-253">Коды возврата для поведения после установки.</span><span class="sxs-lookup"><span data-stu-id="2e057-253">The return codes for post installation behavior.</span></span>|
|<span data-ttu-id="2e057-254">мсиинформатион</span><span class="sxs-lookup"><span data-stu-id="2e057-254">msiInformation</span></span>|[<span data-ttu-id="2e057-255">win32LobAppMsiInformation</span><span class="sxs-lookup"><span data-stu-id="2e057-255">win32LobAppMsiInformation</span></span>](../resources/intune-apps-win32lobappmsiinformation.md)|<span data-ttu-id="2e057-256">Сведения о MSI, если это приложение Win32 является приложением MSI.</span><span class="sxs-lookup"><span data-stu-id="2e057-256">The MSI details if this Win32 app is an MSI app.</span></span>|
|<span data-ttu-id="2e057-257">сетупфилепас</span><span class="sxs-lookup"><span data-stu-id="2e057-257">setupFilePath</span></span>|<span data-ttu-id="2e057-258">String.</span><span class="sxs-lookup"><span data-stu-id="2e057-258">String</span></span>|<span data-ttu-id="2e057-259">Относительный путь к файлу установки в зашифрованном пакете Win32LobApp.</span><span class="sxs-lookup"><span data-stu-id="2e057-259">The relative path of the setup file in the encrypted Win32LobApp package.</span></span>|



## <a name="response"></a><span data-ttu-id="2e057-260">Отклик</span><span class="sxs-lookup"><span data-stu-id="2e057-260">Response</span></span>
<span data-ttu-id="2e057-261">В случае успешного выполнения этот метод возвращает `201 Created` код отклика и объект [win32LobApp](../resources/intune-apps-win32lobapp.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="2e057-261">If successful, this method returns a `201 Created` response code and a [win32LobApp](../resources/intune-apps-win32lobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2e057-262">Пример</span><span class="sxs-lookup"><span data-stu-id="2e057-262">Example</span></span>

### <a name="request"></a><span data-ttu-id="2e057-263">Запрос</span><span class="sxs-lookup"><span data-stu-id="2e057-263">Request</span></span>
<span data-ttu-id="2e057-264">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="2e057-264">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 2778

{
  "@odata.type": "#microsoft.graph.win32LobApp",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "uploadState": 11,
  "publishingState": "processing",
  "isAssigned": true,
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "dependentAppCount": 1,
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "installCommandLine": "Install Command Line value",
  "uninstallCommandLine": "Uninstall Command Line value",
  "applicableArchitectures": "x86",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true,
    "v10_1809": true,
    "v10_1903": true
  },
  "minimumFreeDiskSpaceInMB": 8,
  "minimumMemoryInMB": 1,
  "minimumNumberOfProcessors": 9,
  "minimumCpuSpeedInMHz": 4,
  "detectionRules": [
    {
      "@odata.type": "microsoft.graph.win32LobAppRegistryDetection",
      "check32BitOn64System": true,
      "keyPath": "Key Path value",
      "valueName": "Value Name value",
      "detectionType": "exists",
      "operator": "equal",
      "detectionValue": "Detection Value value"
    }
  ],
  "requirementRules": [
    {
      "@odata.type": "microsoft.graph.win32LobAppRegistryRequirement",
      "operator": "equal",
      "detectionValue": "Detection Value value",
      "check32BitOn64System": true,
      "keyPath": "Key Path value",
      "valueName": "Value Name value",
      "detectionType": "exists"
    }
  ],
  "installExperience": {
    "@odata.type": "microsoft.graph.win32LobAppInstallExperience",
    "runAsAccount": "user"
  },
  "returnCodes": [
    {
      "@odata.type": "microsoft.graph.win32LobAppReturnCode",
      "returnCode": 10,
      "type": "success"
    }
  ],
  "msiInformation": {
    "@odata.type": "microsoft.graph.win32LobAppMsiInformation",
    "productCode": "Product Code value",
    "productVersion": "Product Version value",
    "upgradeCode": "Upgrade Code value",
    "requiresReboot": true,
    "packageType": "perUser",
    "productName": "Product Name value",
    "publisher": "Publisher value"
  },
  "setupFilePath": "Setup File Path value"
}
```

### <a name="response"></a><span data-ttu-id="2e057-265">Отклик</span><span class="sxs-lookup"><span data-stu-id="2e057-265">Response</span></span>
<span data-ttu-id="2e057-p123">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="2e057-p123">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 2950

{
  "@odata.type": "#microsoft.graph.win32LobApp",
  "id": "9607b530-b530-9607-30b5-079630b50796",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "uploadState": 11,
  "publishingState": "processing",
  "isAssigned": true,
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "dependentAppCount": 1,
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "installCommandLine": "Install Command Line value",
  "uninstallCommandLine": "Uninstall Command Line value",
  "applicableArchitectures": "x86",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true,
    "v10_1809": true,
    "v10_1903": true
  },
  "minimumFreeDiskSpaceInMB": 8,
  "minimumMemoryInMB": 1,
  "minimumNumberOfProcessors": 9,
  "minimumCpuSpeedInMHz": 4,
  "detectionRules": [
    {
      "@odata.type": "microsoft.graph.win32LobAppRegistryDetection",
      "check32BitOn64System": true,
      "keyPath": "Key Path value",
      "valueName": "Value Name value",
      "detectionType": "exists",
      "operator": "equal",
      "detectionValue": "Detection Value value"
    }
  ],
  "requirementRules": [
    {
      "@odata.type": "microsoft.graph.win32LobAppRegistryRequirement",
      "operator": "equal",
      "detectionValue": "Detection Value value",
      "check32BitOn64System": true,
      "keyPath": "Key Path value",
      "valueName": "Value Name value",
      "detectionType": "exists"
    }
  ],
  "installExperience": {
    "@odata.type": "microsoft.graph.win32LobAppInstallExperience",
    "runAsAccount": "user"
  },
  "returnCodes": [
    {
      "@odata.type": "microsoft.graph.win32LobAppReturnCode",
      "returnCode": 10,
      "type": "success"
    }
  ],
  "msiInformation": {
    "@odata.type": "microsoft.graph.win32LobAppMsiInformation",
    "productCode": "Product Code value",
    "productVersion": "Product Version value",
    "upgradeCode": "Upgrade Code value",
    "requiresReboot": true,
    "packageType": "perUser",
    "productName": "Product Name value",
    "publisher": "Publisher value"
  },
  "setupFilePath": "Setup File Path value"
}
```




