---
title: Создание Андроидманажедстореапп
description: Создание нового объекта Андроидманажедстореапп.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: 8735f1d09b2e6296e79753e7ce73356d6da979aa
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48012371"
---
# <a name="create-androidmanagedstoreapp"></a><span data-ttu-id="4b853-103">Создание Андроидманажедстореапп</span><span class="sxs-lookup"><span data-stu-id="4b853-103">Create androidManagedStoreApp</span></span>

<span data-ttu-id="4b853-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="4b853-104">Namespace: microsoft.graph</span></span>

> <span data-ttu-id="4b853-105">**Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4b853-105">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="4b853-106">**Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="4b853-106">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="4b853-107">Создание нового объекта [андроидманажедстореапп](../resources/intune-apps-androidmanagedstoreapp.md) .</span><span class="sxs-lookup"><span data-stu-id="4b853-107">Create a new [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4b853-108">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="4b853-108">Prerequisites</span></span>
<span data-ttu-id="4b853-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4b853-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4b853-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="4b853-111">Permission type</span></span>|<span data-ttu-id="4b853-112">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="4b853-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4b853-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="4b853-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4b853-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4b853-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="4b853-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="4b853-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4b853-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4b853-116">Not supported.</span></span>|
|<span data-ttu-id="4b853-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="4b853-117">Application</span></span>|<span data-ttu-id="4b853-118">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4b853-118">DeviceManagementApps.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="4b853-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="4b853-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="4b853-120">Заголовки запроса</span><span class="sxs-lookup"><span data-stu-id="4b853-120">Request headers</span></span>
|<span data-ttu-id="4b853-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4b853-121">Header</span></span>|<span data-ttu-id="4b853-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4b853-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4b853-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4b853-123">Authorization</span></span>|<span data-ttu-id="4b853-124">Bearer &lt;token&gt;. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4b853-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4b853-125">Accept</span><span class="sxs-lookup"><span data-stu-id="4b853-125">Accept</span></span>|<span data-ttu-id="4b853-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4b853-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4b853-127">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="4b853-127">Request body</span></span>
<span data-ttu-id="4b853-128">В тексте запроса добавьте представление объекта Андроидманажедстореапп в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="4b853-128">In the request body, supply a JSON representation for the androidManagedStoreApp object.</span></span>

<span data-ttu-id="4b853-129">В следующей таблице приведены свойства, необходимые при создании Андроидманажедстореапп.</span><span class="sxs-lookup"><span data-stu-id="4b853-129">The following table shows the properties that are required when you create the androidManagedStoreApp.</span></span>

|<span data-ttu-id="4b853-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="4b853-130">Property</span></span>|<span data-ttu-id="4b853-131">Тип</span><span class="sxs-lookup"><span data-stu-id="4b853-131">Type</span></span>|<span data-ttu-id="4b853-132">Описание</span><span class="sxs-lookup"><span data-stu-id="4b853-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4b853-133">id</span><span class="sxs-lookup"><span data-stu-id="4b853-133">id</span></span>|<span data-ttu-id="4b853-134">String</span><span class="sxs-lookup"><span data-stu-id="4b853-134">String</span></span>|<span data-ttu-id="4b853-135">Ключ объекта.</span><span class="sxs-lookup"><span data-stu-id="4b853-135">Key of the entity.</span></span> <span data-ttu-id="4b853-136">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-136">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-137">displayName</span><span class="sxs-lookup"><span data-stu-id="4b853-137">displayName</span></span>|<span data-ttu-id="4b853-138">String</span><span class="sxs-lookup"><span data-stu-id="4b853-138">String</span></span>|<span data-ttu-id="4b853-139">Название приложения, которое предоставил или импортировал администратор.</span><span class="sxs-lookup"><span data-stu-id="4b853-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="4b853-140">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-140">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-141">description</span><span class="sxs-lookup"><span data-stu-id="4b853-141">description</span></span>|<span data-ttu-id="4b853-142">String</span><span class="sxs-lookup"><span data-stu-id="4b853-142">String</span></span>|<span data-ttu-id="4b853-143">Описание приложения.</span><span class="sxs-lookup"><span data-stu-id="4b853-143">The description of the app.</span></span> <span data-ttu-id="4b853-144">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-144">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-145">publisher</span><span class="sxs-lookup"><span data-stu-id="4b853-145">publisher</span></span>|<span data-ttu-id="4b853-146">String</span><span class="sxs-lookup"><span data-stu-id="4b853-146">String</span></span>|<span data-ttu-id="4b853-147">Издатель приложения.</span><span class="sxs-lookup"><span data-stu-id="4b853-147">The publisher of the app.</span></span> <span data-ttu-id="4b853-148">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-148">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="4b853-149">largeIcon</span></span>|[<span data-ttu-id="4b853-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="4b853-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="4b853-151">Представляет большой значок, который отображается в сведениях о приложении, используется для отправки значка.</span><span class="sxs-lookup"><span data-stu-id="4b853-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="4b853-152">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-152">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4b853-153">createdDateTime</span></span>|<span data-ttu-id="4b853-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4b853-154">DateTimeOffset</span></span>|<span data-ttu-id="4b853-155">Дата и время создания приложения.</span><span class="sxs-lookup"><span data-stu-id="4b853-155">The date and time the app was created.</span></span> <span data-ttu-id="4b853-156">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-156">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4b853-157">lastModifiedDateTime</span></span>|<span data-ttu-id="4b853-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4b853-158">DateTimeOffset</span></span>|<span data-ttu-id="4b853-159">Дата и время последнего изменения приложения.</span><span class="sxs-lookup"><span data-stu-id="4b853-159">The date and time the app was last modified.</span></span> <span data-ttu-id="4b853-160">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-160">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="4b853-161">isFeatured</span></span>|<span data-ttu-id="4b853-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="4b853-162">Boolean</span></span>|<span data-ttu-id="4b853-163">Значение, которое показывает, отмечено ли приложение как подобранное администратором. Наследуется от объекта [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="4b853-164">privacyInformationUrl</span></span>|<span data-ttu-id="4b853-165">String</span><span class="sxs-lookup"><span data-stu-id="4b853-165">String</span></span>|<span data-ttu-id="4b853-166">URL-адрес заявления о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="4b853-166">The privacy statement Url.</span></span> <span data-ttu-id="4b853-167">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-167">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="4b853-168">informationUrl</span></span>|<span data-ttu-id="4b853-169">String</span><span class="sxs-lookup"><span data-stu-id="4b853-169">String</span></span>|<span data-ttu-id="4b853-170">URL-адрес страницы с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="4b853-170">The more information Url.</span></span> <span data-ttu-id="4b853-171">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-171">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-172">owner</span><span class="sxs-lookup"><span data-stu-id="4b853-172">owner</span></span>|<span data-ttu-id="4b853-173">String</span><span class="sxs-lookup"><span data-stu-id="4b853-173">String</span></span>|<span data-ttu-id="4b853-174">Владелец приложения.</span><span class="sxs-lookup"><span data-stu-id="4b853-174">The owner of the app.</span></span> <span data-ttu-id="4b853-175">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-175">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-176">developer</span><span class="sxs-lookup"><span data-stu-id="4b853-176">developer</span></span>|<span data-ttu-id="4b853-177">String</span><span class="sxs-lookup"><span data-stu-id="4b853-177">String</span></span>|<span data-ttu-id="4b853-178">Разработчик приложения.</span><span class="sxs-lookup"><span data-stu-id="4b853-178">The developer of the app.</span></span> <span data-ttu-id="4b853-179">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-179">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-180">notes</span><span class="sxs-lookup"><span data-stu-id="4b853-180">notes</span></span>|<span data-ttu-id="4b853-181">String</span><span class="sxs-lookup"><span data-stu-id="4b853-181">String</span></span>|<span data-ttu-id="4b853-182">Заметки для приложения.</span><span class="sxs-lookup"><span data-stu-id="4b853-182">Notes for the app.</span></span> <span data-ttu-id="4b853-183">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-183">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="4b853-184">uploadState</span></span>|<span data-ttu-id="4b853-185">Int32</span><span class="sxs-lookup"><span data-stu-id="4b853-185">Int32</span></span>|<span data-ttu-id="4b853-186">Состояние отправки.</span><span class="sxs-lookup"><span data-stu-id="4b853-186">The upload state.</span></span> <span data-ttu-id="4b853-187">Возможные значения: 0 – `Not Ready` , 1 – `Ready` , 2 `Processing` .</span><span class="sxs-lookup"><span data-stu-id="4b853-187">Possible values are: 0 - `Not Ready`, 1 - `Ready`, 2 - `Processing`.</span></span> <span data-ttu-id="4b853-188">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-188">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-189">publishingState</span><span class="sxs-lookup"><span data-stu-id="4b853-189">publishingState</span></span>|[<span data-ttu-id="4b853-190">мобилеапппублишингстате</span><span class="sxs-lookup"><span data-stu-id="4b853-190">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="4b853-191">Состояние публикации для приложения.</span><span class="sxs-lookup"><span data-stu-id="4b853-191">The publishing state for the app.</span></span> <span data-ttu-id="4b853-192">Приложение невозможно назначить, если оно не опубликовано.</span><span class="sxs-lookup"><span data-stu-id="4b853-192">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="4b853-193">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-193">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md).</span></span> <span data-ttu-id="4b853-194">Возможные значения: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="4b853-194">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="4b853-195">isAssigned</span><span class="sxs-lookup"><span data-stu-id="4b853-195">isAssigned</span></span>|<span data-ttu-id="4b853-196">Boolean</span><span class="sxs-lookup"><span data-stu-id="4b853-196">Boolean</span></span>|<span data-ttu-id="4b853-197">Значение, указывающее, назначено ли приложение по крайней мере одной группе.</span><span class="sxs-lookup"><span data-stu-id="4b853-197">The value indicating whether the app is assigned to at least one group.</span></span> <span data-ttu-id="4b853-198">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-198">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-199">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="4b853-199">roleScopeTagIds</span></span>|<span data-ttu-id="4b853-200">Коллекция String</span><span class="sxs-lookup"><span data-stu-id="4b853-200">String collection</span></span>|<span data-ttu-id="4b853-201">Список идентификаторов тегов области для этого мобильного приложения.</span><span class="sxs-lookup"><span data-stu-id="4b853-201">List of scope tag ids for this mobile app.</span></span> <span data-ttu-id="4b853-202">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-202">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-203">депендентаппкаунт</span><span class="sxs-lookup"><span data-stu-id="4b853-203">dependentAppCount</span></span>|<span data-ttu-id="4b853-204">Int32</span><span class="sxs-lookup"><span data-stu-id="4b853-204">Int32</span></span>|<span data-ttu-id="4b853-205">Общее количество зависимостей для дочернего приложения.</span><span class="sxs-lookup"><span data-stu-id="4b853-205">The total number of dependencies the child app has.</span></span> <span data-ttu-id="4b853-206">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-206">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-207">суперседингаппкаунт</span><span class="sxs-lookup"><span data-stu-id="4b853-207">supersedingAppCount</span></span>|<span data-ttu-id="4b853-208">Int32</span><span class="sxs-lookup"><span data-stu-id="4b853-208">Int32</span></span>|<span data-ttu-id="4b853-209">Общее количество приложений, которые напрямую или косвенно заменяют данное приложение.</span><span class="sxs-lookup"><span data-stu-id="4b853-209">The total number of apps this app directly or indirectly supersedes.</span></span> <span data-ttu-id="4b853-210">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-210">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-211">суперседедаппкаунт</span><span class="sxs-lookup"><span data-stu-id="4b853-211">supersededAppCount</span></span>|<span data-ttu-id="4b853-212">Int32</span><span class="sxs-lookup"><span data-stu-id="4b853-212">Int32</span></span>|<span data-ttu-id="4b853-213">Общее число приложений, для которых это приложение напрямую или косвенно заменяется.</span><span class="sxs-lookup"><span data-stu-id="4b853-213">The total number of apps this app is directly or indirectly superseded by.</span></span> <span data-ttu-id="4b853-214">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4b853-214">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="4b853-215">packageId</span><span class="sxs-lookup"><span data-stu-id="4b853-215">packageId</span></span>|<span data-ttu-id="4b853-216">String</span><span class="sxs-lookup"><span data-stu-id="4b853-216">String</span></span>|<span data-ttu-id="4b853-217">Идентификатор пакета.</span><span class="sxs-lookup"><span data-stu-id="4b853-217">The package identifier.</span></span>|
|<span data-ttu-id="4b853-218">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="4b853-218">appIdentifier</span></span>|<span data-ttu-id="4b853-219">String</span><span class="sxs-lookup"><span data-stu-id="4b853-219">String</span></span>|<span data-ttu-id="4b853-220">Имя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="4b853-220">The Identity Name.</span></span>|
|<span data-ttu-id="4b853-221">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="4b853-221">usedLicenseCount</span></span>|<span data-ttu-id="4b853-222">Int32</span><span class="sxs-lookup"><span data-stu-id="4b853-222">Int32</span></span>|<span data-ttu-id="4b853-223">Количество используемых лицензий VPP.</span><span class="sxs-lookup"><span data-stu-id="4b853-223">The number of VPP licenses in use.</span></span>|
|<span data-ttu-id="4b853-224">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="4b853-224">totalLicenseCount</span></span>|<span data-ttu-id="4b853-225">Int32</span><span class="sxs-lookup"><span data-stu-id="4b853-225">Int32</span></span>|<span data-ttu-id="4b853-226">Общее количество лицензий VPP.</span><span class="sxs-lookup"><span data-stu-id="4b853-226">The total number of VPP licenses.</span></span>|
|<span data-ttu-id="4b853-227">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="4b853-227">appStoreUrl</span></span>|<span data-ttu-id="4b853-228">String</span><span class="sxs-lookup"><span data-stu-id="4b853-228">String</span></span>|<span data-ttu-id="4b853-229">URL-адрес приложения для рабочего хранилища.</span><span class="sxs-lookup"><span data-stu-id="4b853-229">The Play for Work Store app URL.</span></span>|
|<span data-ttu-id="4b853-230">Частный</span><span class="sxs-lookup"><span data-stu-id="4b853-230">isPrivate</span></span>|<span data-ttu-id="4b853-231">Boolean</span><span class="sxs-lookup"><span data-stu-id="4b853-231">Boolean</span></span>|<span data-ttu-id="4b853-232">Указывает, доступно ли приложение только для указанных пользователей предприятия.</span><span class="sxs-lookup"><span data-stu-id="4b853-232">Indicates whether the app is only available to a given enterprise's users.</span></span>|
|<span data-ttu-id="4b853-233">иссистемапп</span><span class="sxs-lookup"><span data-stu-id="4b853-233">isSystemApp</span></span>|<span data-ttu-id="4b853-234">Boolean</span><span class="sxs-lookup"><span data-stu-id="4b853-234">Boolean</span></span>|<span data-ttu-id="4b853-235">Указывает, является ли приложение предустановленным системным приложением.</span><span class="sxs-lookup"><span data-stu-id="4b853-235">Indicates whether the app is a preinstalled system app.</span></span>|
|<span data-ttu-id="4b853-236">апптраккс</span><span class="sxs-lookup"><span data-stu-id="4b853-236">appTracks</span></span>|<span data-ttu-id="4b853-237">Коллекция [андроидманажедстореапптракк](../resources/intune-apps-androidmanagedstoreapptrack.md)</span><span class="sxs-lookup"><span data-stu-id="4b853-237">[androidManagedStoreAppTrack](../resources/intune-apps-androidmanagedstoreapptrack.md) collection</span></span>|<span data-ttu-id="4b853-238">Дорожки, которые видимы для этого предприятия.</span><span class="sxs-lookup"><span data-stu-id="4b853-238">The tracks that are visible to this enterprise.</span></span>|
|<span data-ttu-id="4b853-239">суппортсоемконфиг</span><span class="sxs-lookup"><span data-stu-id="4b853-239">supportsOemConfig</span></span>|<span data-ttu-id="4b853-240">Boolean</span><span class="sxs-lookup"><span data-stu-id="4b853-240">Boolean</span></span>|<span data-ttu-id="4b853-241">Поддерживает ли это приложение политику Оемконфиг.</span><span class="sxs-lookup"><span data-stu-id="4b853-241">Whether this app supports OEMConfig policy.</span></span>|



## <a name="response"></a><span data-ttu-id="4b853-242">Отклик</span><span class="sxs-lookup"><span data-stu-id="4b853-242">Response</span></span>
<span data-ttu-id="4b853-243">В случае успешного выполнения этот метод возвращает `201 Created` код отклика и объект [андроидманажедстореапп](../resources/intune-apps-androidmanagedstoreapp.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="4b853-243">If successful, this method returns a `201 Created` response code and a [androidManagedStoreApp](../resources/intune-apps-androidmanagedstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4b853-244">Пример</span><span class="sxs-lookup"><span data-stu-id="4b853-244">Example</span></span>

### <a name="request"></a><span data-ttu-id="4b853-245">Запрос</span><span class="sxs-lookup"><span data-stu-id="4b853-245">Request</span></span>
<span data-ttu-id="4b853-246">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="4b853-246">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1225

{
  "@odata.type": "#microsoft.graph.androidManagedStoreApp",
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
  "supersedingAppCount": 3,
  "supersededAppCount": 2,
  "packageId": "Package Id value",
  "appIdentifier": "App Identifier value",
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "isPrivate": true,
  "isSystemApp": true,
  "appTracks": [
    {
      "@odata.type": "microsoft.graph.androidManagedStoreAppTrack",
      "trackId": "Track Id value",
      "trackAlias": "Track Alias value"
    }
  ],
  "supportsOemConfig": true
}
```

### <a name="response"></a><span data-ttu-id="4b853-247">Отклик</span><span class="sxs-lookup"><span data-stu-id="4b853-247">Response</span></span>
<span data-ttu-id="4b853-p121">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="4b853-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1397

{
  "@odata.type": "#microsoft.graph.androidManagedStoreApp",
  "id": "87247525-7525-8724-2575-248725752487",
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
  "supersedingAppCount": 3,
  "supersededAppCount": 2,
  "packageId": "Package Id value",
  "appIdentifier": "App Identifier value",
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "isPrivate": true,
  "isSystemApp": true,
  "appTracks": [
    {
      "@odata.type": "microsoft.graph.androidManagedStoreAppTrack",
      "trackId": "Track Id value",
      "trackAlias": "Track Alias value"
    }
  ],
  "supportsOemConfig": true
}
```






