---
title: Update iosStoreApp
description: Обновление свойств объекта iosStoreApp.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: dc32aff8c35c38805c8080b158af16b29e278d22
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48001045"
---
# <a name="update-iosstoreapp"></a><span data-ttu-id="078f2-103">Update iosStoreApp</span><span class="sxs-lookup"><span data-stu-id="078f2-103">Update iosStoreApp</span></span>

<span data-ttu-id="078f2-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="078f2-104">Namespace: microsoft.graph</span></span>

> <span data-ttu-id="078f2-105">**Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="078f2-105">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="078f2-106">**Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="078f2-106">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="078f2-107">Обновление свойств объекта [iosStoreApp](../resources/intune-apps-iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-107">Update the properties of a [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="078f2-108">Необходимые разрешения</span><span class="sxs-lookup"><span data-stu-id="078f2-108">Prerequisites</span></span>
<span data-ttu-id="078f2-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="078f2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="078f2-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="078f2-111">Permission type</span></span>|<span data-ttu-id="078f2-112">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="078f2-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="078f2-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="078f2-113">Delegated (work or school account)</span></span>|<span data-ttu-id="078f2-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="078f2-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="078f2-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="078f2-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="078f2-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="078f2-116">Not supported.</span></span>|
|<span data-ttu-id="078f2-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="078f2-117">Application</span></span>|<span data-ttu-id="078f2-118">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="078f2-118">DeviceManagementApps.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="078f2-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="078f2-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="078f2-120">Заголовки запроса</span><span class="sxs-lookup"><span data-stu-id="078f2-120">Request headers</span></span>
|<span data-ttu-id="078f2-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="078f2-121">Header</span></span>|<span data-ttu-id="078f2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="078f2-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="078f2-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="078f2-123">Authorization</span></span>|<span data-ttu-id="078f2-124">Bearer &lt;token&gt;. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="078f2-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="078f2-125">Accept</span><span class="sxs-lookup"><span data-stu-id="078f2-125">Accept</span></span>|<span data-ttu-id="078f2-126">application/json</span><span class="sxs-lookup"><span data-stu-id="078f2-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="078f2-127">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="078f2-127">Request body</span></span>
<span data-ttu-id="078f2-128">В тексте запроса добавьте представление объекта [iosStoreApp](../resources/intune-apps-iosstoreapp.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="078f2-128">In the request body, supply a JSON representation for the [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object.</span></span>

<span data-ttu-id="078f2-129">В приведенной ниже таблице показаны свойства, которые необходимо указывать при создании объекта [iosStoreApp](../resources/intune-apps-iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-129">The following table shows the properties that are required when you create the [iosStoreApp](../resources/intune-apps-iosstoreapp.md).</span></span>

|<span data-ttu-id="078f2-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="078f2-130">Property</span></span>|<span data-ttu-id="078f2-131">Тип</span><span class="sxs-lookup"><span data-stu-id="078f2-131">Type</span></span>|<span data-ttu-id="078f2-132">Описание</span><span class="sxs-lookup"><span data-stu-id="078f2-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="078f2-133">id</span><span class="sxs-lookup"><span data-stu-id="078f2-133">id</span></span>|<span data-ttu-id="078f2-134">String</span><span class="sxs-lookup"><span data-stu-id="078f2-134">String</span></span>|<span data-ttu-id="078f2-135">Ключ объекта.</span><span class="sxs-lookup"><span data-stu-id="078f2-135">Key of the entity.</span></span> <span data-ttu-id="078f2-136">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-136">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-137">displayName</span><span class="sxs-lookup"><span data-stu-id="078f2-137">displayName</span></span>|<span data-ttu-id="078f2-138">String</span><span class="sxs-lookup"><span data-stu-id="078f2-138">String</span></span>|<span data-ttu-id="078f2-139">Название приложения, которое предоставил или импортировал администратор.</span><span class="sxs-lookup"><span data-stu-id="078f2-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="078f2-140">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-140">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-141">description</span><span class="sxs-lookup"><span data-stu-id="078f2-141">description</span></span>|<span data-ttu-id="078f2-142">String</span><span class="sxs-lookup"><span data-stu-id="078f2-142">String</span></span>|<span data-ttu-id="078f2-143">Описание приложения.</span><span class="sxs-lookup"><span data-stu-id="078f2-143">The description of the app.</span></span> <span data-ttu-id="078f2-144">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-144">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-145">publisher</span><span class="sxs-lookup"><span data-stu-id="078f2-145">publisher</span></span>|<span data-ttu-id="078f2-146">String</span><span class="sxs-lookup"><span data-stu-id="078f2-146">String</span></span>|<span data-ttu-id="078f2-147">Издатель приложения.</span><span class="sxs-lookup"><span data-stu-id="078f2-147">The publisher of the app.</span></span> <span data-ttu-id="078f2-148">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-148">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="078f2-149">largeIcon</span></span>|[<span data-ttu-id="078f2-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="078f2-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="078f2-151">Представляет большой значок, который отображается в сведениях о приложении, используется для отправки значка.</span><span class="sxs-lookup"><span data-stu-id="078f2-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="078f2-152">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-152">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="078f2-153">createdDateTime</span></span>|<span data-ttu-id="078f2-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="078f2-154">DateTimeOffset</span></span>|<span data-ttu-id="078f2-155">Дата и время создания приложения.</span><span class="sxs-lookup"><span data-stu-id="078f2-155">The date and time the app was created.</span></span> <span data-ttu-id="078f2-156">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-156">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="078f2-157">lastModifiedDateTime</span></span>|<span data-ttu-id="078f2-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="078f2-158">DateTimeOffset</span></span>|<span data-ttu-id="078f2-159">Дата и время последнего изменения приложения.</span><span class="sxs-lookup"><span data-stu-id="078f2-159">The date and time the app was last modified.</span></span> <span data-ttu-id="078f2-160">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-160">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="078f2-161">isFeatured</span></span>|<span data-ttu-id="078f2-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="078f2-162">Boolean</span></span>|<span data-ttu-id="078f2-163">Значение, которое показывает, отмечено ли приложение как подобранное администратором. Наследуется от объекта [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="078f2-164">privacyInformationUrl</span></span>|<span data-ttu-id="078f2-165">String</span><span class="sxs-lookup"><span data-stu-id="078f2-165">String</span></span>|<span data-ttu-id="078f2-166">URL-адрес заявления о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="078f2-166">The privacy statement Url.</span></span> <span data-ttu-id="078f2-167">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-167">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="078f2-168">informationUrl</span></span>|<span data-ttu-id="078f2-169">String</span><span class="sxs-lookup"><span data-stu-id="078f2-169">String</span></span>|<span data-ttu-id="078f2-170">URL-адрес страницы с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="078f2-170">The more information Url.</span></span> <span data-ttu-id="078f2-171">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-171">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-172">owner</span><span class="sxs-lookup"><span data-stu-id="078f2-172">owner</span></span>|<span data-ttu-id="078f2-173">String</span><span class="sxs-lookup"><span data-stu-id="078f2-173">String</span></span>|<span data-ttu-id="078f2-174">Владелец приложения.</span><span class="sxs-lookup"><span data-stu-id="078f2-174">The owner of the app.</span></span> <span data-ttu-id="078f2-175">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-175">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-176">developer</span><span class="sxs-lookup"><span data-stu-id="078f2-176">developer</span></span>|<span data-ttu-id="078f2-177">String</span><span class="sxs-lookup"><span data-stu-id="078f2-177">String</span></span>|<span data-ttu-id="078f2-178">Разработчик приложения.</span><span class="sxs-lookup"><span data-stu-id="078f2-178">The developer of the app.</span></span> <span data-ttu-id="078f2-179">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-179">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-180">notes</span><span class="sxs-lookup"><span data-stu-id="078f2-180">notes</span></span>|<span data-ttu-id="078f2-181">String</span><span class="sxs-lookup"><span data-stu-id="078f2-181">String</span></span>|<span data-ttu-id="078f2-182">Заметки для приложения.</span><span class="sxs-lookup"><span data-stu-id="078f2-182">Notes for the app.</span></span> <span data-ttu-id="078f2-183">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-183">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="078f2-184">uploadState</span></span>|<span data-ttu-id="078f2-185">Int32</span><span class="sxs-lookup"><span data-stu-id="078f2-185">Int32</span></span>|<span data-ttu-id="078f2-186">Состояние отправки.</span><span class="sxs-lookup"><span data-stu-id="078f2-186">The upload state.</span></span> <span data-ttu-id="078f2-187">Возможные значения: 0 – `Not Ready` , 1 – `Ready` , 2 `Processing` .</span><span class="sxs-lookup"><span data-stu-id="078f2-187">Possible values are: 0 - `Not Ready`, 1 - `Ready`, 2 - `Processing`.</span></span> <span data-ttu-id="078f2-188">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-188">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-189">publishingState</span><span class="sxs-lookup"><span data-stu-id="078f2-189">publishingState</span></span>|[<span data-ttu-id="078f2-190">мобилеапппублишингстате</span><span class="sxs-lookup"><span data-stu-id="078f2-190">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="078f2-191">Состояние публикации для приложения.</span><span class="sxs-lookup"><span data-stu-id="078f2-191">The publishing state for the app.</span></span> <span data-ttu-id="078f2-192">Приложение невозможно назначить, если оно не опубликовано.</span><span class="sxs-lookup"><span data-stu-id="078f2-192">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="078f2-193">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-193">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md).</span></span> <span data-ttu-id="078f2-194">Возможные значения: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="078f2-194">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="078f2-195">isAssigned</span><span class="sxs-lookup"><span data-stu-id="078f2-195">isAssigned</span></span>|<span data-ttu-id="078f2-196">Boolean</span><span class="sxs-lookup"><span data-stu-id="078f2-196">Boolean</span></span>|<span data-ttu-id="078f2-197">Значение, указывающее, назначено ли приложение по крайней мере одной группе.</span><span class="sxs-lookup"><span data-stu-id="078f2-197">The value indicating whether the app is assigned to at least one group.</span></span> <span data-ttu-id="078f2-198">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-198">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-199">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="078f2-199">roleScopeTagIds</span></span>|<span data-ttu-id="078f2-200">Коллекция String</span><span class="sxs-lookup"><span data-stu-id="078f2-200">String collection</span></span>|<span data-ttu-id="078f2-201">Список идентификаторов тегов области для этого мобильного приложения.</span><span class="sxs-lookup"><span data-stu-id="078f2-201">List of scope tag ids for this mobile app.</span></span> <span data-ttu-id="078f2-202">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-202">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-203">депендентаппкаунт</span><span class="sxs-lookup"><span data-stu-id="078f2-203">dependentAppCount</span></span>|<span data-ttu-id="078f2-204">Int32</span><span class="sxs-lookup"><span data-stu-id="078f2-204">Int32</span></span>|<span data-ttu-id="078f2-205">Общее количество зависимостей для дочернего приложения.</span><span class="sxs-lookup"><span data-stu-id="078f2-205">The total number of dependencies the child app has.</span></span> <span data-ttu-id="078f2-206">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-206">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-207">суперседингаппкаунт</span><span class="sxs-lookup"><span data-stu-id="078f2-207">supersedingAppCount</span></span>|<span data-ttu-id="078f2-208">Int32</span><span class="sxs-lookup"><span data-stu-id="078f2-208">Int32</span></span>|<span data-ttu-id="078f2-209">Общее количество приложений, которые напрямую или косвенно заменяют данное приложение.</span><span class="sxs-lookup"><span data-stu-id="078f2-209">The total number of apps this app directly or indirectly supersedes.</span></span> <span data-ttu-id="078f2-210">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-210">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-211">суперседедаппкаунт</span><span class="sxs-lookup"><span data-stu-id="078f2-211">supersededAppCount</span></span>|<span data-ttu-id="078f2-212">Int32</span><span class="sxs-lookup"><span data-stu-id="078f2-212">Int32</span></span>|<span data-ttu-id="078f2-213">Общее число приложений, для которых это приложение напрямую или косвенно заменяется.</span><span class="sxs-lookup"><span data-stu-id="078f2-213">The total number of apps this app is directly or indirectly superseded by.</span></span> <span data-ttu-id="078f2-214">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="078f2-214">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="078f2-215">bundleId</span><span class="sxs-lookup"><span data-stu-id="078f2-215">bundleId</span></span>|<span data-ttu-id="078f2-216">String</span><span class="sxs-lookup"><span data-stu-id="078f2-216">String</span></span>|<span data-ttu-id="078f2-217">Имя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="078f2-217">The Identity Name.</span></span>|
|<span data-ttu-id="078f2-218">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="078f2-218">appStoreUrl</span></span>|<span data-ttu-id="078f2-219">String</span><span class="sxs-lookup"><span data-stu-id="078f2-219">String</span></span>|<span data-ttu-id="078f2-220">URL-адрес в Apple App Store</span><span class="sxs-lookup"><span data-stu-id="078f2-220">The Apple App Store URL</span></span>|
|<span data-ttu-id="078f2-221">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="078f2-221">applicableDeviceType</span></span>|[<span data-ttu-id="078f2-222">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="078f2-222">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="078f2-223">Архитектура iOS, которая поддерживается этим приложением.</span><span class="sxs-lookup"><span data-stu-id="078f2-223">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="078f2-224">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="078f2-224">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="078f2-225">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="078f2-225">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="078f2-226">Значение, которое представляет минимальную применимую версию операционной системы.</span><span class="sxs-lookup"><span data-stu-id="078f2-226">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="078f2-227">Ответ</span><span class="sxs-lookup"><span data-stu-id="078f2-227">Response</span></span>
<span data-ttu-id="078f2-228">В случае успешного выполнения этот метод возвращает код ответа `200 OK` и обновленный объект [iosStoreApp](../resources/intune-apps-iosstoreapp.md) в тексте ответа.</span><span class="sxs-lookup"><span data-stu-id="078f2-228">If successful, this method returns a `200 OK` response code and an updated [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="078f2-229">Пример</span><span class="sxs-lookup"><span data-stu-id="078f2-229">Example</span></span>

### <a name="request"></a><span data-ttu-id="078f2-230">Запрос</span><span class="sxs-lookup"><span data-stu-id="078f2-230">Request</span></span>
<span data-ttu-id="078f2-231">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="078f2-231">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1217

{
  "@odata.type": "#microsoft.graph.iosStoreApp",
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
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true,
    "v12_0": true,
    "v13_0": true
  }
}
```

### <a name="response"></a><span data-ttu-id="078f2-232">Отклик</span><span class="sxs-lookup"><span data-stu-id="078f2-232">Response</span></span>
<span data-ttu-id="078f2-p121">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="078f2-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1389

{
  "@odata.type": "#microsoft.graph.iosStoreApp",
  "id": "a04adbe2-dbe2-a04a-e2db-4aa0e2db4aa0",
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
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true,
    "v12_0": true,
    "v13_0": true
  }
}
```






