---
title: Обновление объекта macOSOfficeSuiteApp
description: Обновление свойств объекта macOSOfficeSuiteApp.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: cd1b83b0e92b434d5509e48c030f10298b333e11
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48012035"
---
# <a name="update-macosofficesuiteapp"></a><span data-ttu-id="0a8f5-103">Обновление объекта macOSOfficeSuiteApp</span><span class="sxs-lookup"><span data-stu-id="0a8f5-103">Update macOSOfficeSuiteApp</span></span>

<span data-ttu-id="0a8f5-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="0a8f5-104">Namespace: microsoft.graph</span></span>

> <span data-ttu-id="0a8f5-105">**Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-105">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="0a8f5-106">**Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-106">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="0a8f5-107">Обновление свойств объекта [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-107">Update the properties of a [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0a8f5-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="0a8f5-108">Prerequisites</span></span>
<span data-ttu-id="0a8f5-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0a8f5-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="0a8f5-111">Permission type</span></span>|<span data-ttu-id="0a8f5-112">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="0a8f5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0a8f5-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="0a8f5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0a8f5-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0a8f5-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="0a8f5-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="0a8f5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0a8f5-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-116">Not supported.</span></span>|
|<span data-ttu-id="0a8f5-117">Приложение</span><span class="sxs-lookup"><span data-stu-id="0a8f5-117">Application</span></span>|<span data-ttu-id="0a8f5-118">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0a8f5-118">DeviceManagementApps.ReadWrite.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="0a8f5-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="0a8f5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="0a8f5-120">Заголовки запроса</span><span class="sxs-lookup"><span data-stu-id="0a8f5-120">Request headers</span></span>
|<span data-ttu-id="0a8f5-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0a8f5-121">Header</span></span>|<span data-ttu-id="0a8f5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0a8f5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0a8f5-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0a8f5-123">Authorization</span></span>|<span data-ttu-id="0a8f5-124">Bearer &lt;token&gt;. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0a8f5-125">Accept</span><span class="sxs-lookup"><span data-stu-id="0a8f5-125">Accept</span></span>|<span data-ttu-id="0a8f5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0a8f5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0a8f5-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="0a8f5-127">Request body</span></span>
<span data-ttu-id="0a8f5-128">В тексте запроса добавьте представление объекта [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-128">In the request body, supply a JSON representation for the [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object.</span></span>

<span data-ttu-id="0a8f5-129">В таблице ниже приведены свойства, которые необходимо указывать при создании объекта [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-129">The following table shows the properties that are required when you create the [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span></span>

|<span data-ttu-id="0a8f5-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="0a8f5-130">Property</span></span>|<span data-ttu-id="0a8f5-131">Тип</span><span class="sxs-lookup"><span data-stu-id="0a8f5-131">Type</span></span>|<span data-ttu-id="0a8f5-132">Описание</span><span class="sxs-lookup"><span data-stu-id="0a8f5-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0a8f5-133">id</span><span class="sxs-lookup"><span data-stu-id="0a8f5-133">id</span></span>|<span data-ttu-id="0a8f5-134">String</span><span class="sxs-lookup"><span data-stu-id="0a8f5-134">String</span></span>|<span data-ttu-id="0a8f5-135">Ключ объекта.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-135">Key of the entity.</span></span> <span data-ttu-id="0a8f5-136">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-136">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-137">displayName</span><span class="sxs-lookup"><span data-stu-id="0a8f5-137">displayName</span></span>|<span data-ttu-id="0a8f5-138">String</span><span class="sxs-lookup"><span data-stu-id="0a8f5-138">String</span></span>|<span data-ttu-id="0a8f5-139">Название приложения, которое предоставил или импортировал администратор.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="0a8f5-140">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-140">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-141">description</span><span class="sxs-lookup"><span data-stu-id="0a8f5-141">description</span></span>|<span data-ttu-id="0a8f5-142">String</span><span class="sxs-lookup"><span data-stu-id="0a8f5-142">String</span></span>|<span data-ttu-id="0a8f5-143">Описание приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-143">The description of the app.</span></span> <span data-ttu-id="0a8f5-144">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-144">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-145">publisher</span><span class="sxs-lookup"><span data-stu-id="0a8f5-145">publisher</span></span>|<span data-ttu-id="0a8f5-146">String</span><span class="sxs-lookup"><span data-stu-id="0a8f5-146">String</span></span>|<span data-ttu-id="0a8f5-147">Издатель приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-147">The publisher of the app.</span></span> <span data-ttu-id="0a8f5-148">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-148">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="0a8f5-149">largeIcon</span></span>|[<span data-ttu-id="0a8f5-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="0a8f5-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="0a8f5-151">Представляет большой значок, который отображается в сведениях о приложении, используется для отправки значка.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="0a8f5-152">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-152">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0a8f5-153">createdDateTime</span></span>|<span data-ttu-id="0a8f5-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0a8f5-154">DateTimeOffset</span></span>|<span data-ttu-id="0a8f5-155">Дата и время создания приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-155">The date and time the app was created.</span></span> <span data-ttu-id="0a8f5-156">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-156">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0a8f5-157">lastModifiedDateTime</span></span>|<span data-ttu-id="0a8f5-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0a8f5-158">DateTimeOffset</span></span>|<span data-ttu-id="0a8f5-159">Дата и время последнего изменения приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-159">The date and time the app was last modified.</span></span> <span data-ttu-id="0a8f5-160">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-160">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="0a8f5-161">isFeatured</span></span>|<span data-ttu-id="0a8f5-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="0a8f5-162">Boolean</span></span>|<span data-ttu-id="0a8f5-163">Значение, которое показывает, отмечено ли приложение как подобранное администратором. Наследуется от объекта [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="0a8f5-164">privacyInformationUrl</span></span>|<span data-ttu-id="0a8f5-165">String</span><span class="sxs-lookup"><span data-stu-id="0a8f5-165">String</span></span>|<span data-ttu-id="0a8f5-166">URL-адрес заявления о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-166">The privacy statement Url.</span></span> <span data-ttu-id="0a8f5-167">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-167">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="0a8f5-168">informationUrl</span></span>|<span data-ttu-id="0a8f5-169">String</span><span class="sxs-lookup"><span data-stu-id="0a8f5-169">String</span></span>|<span data-ttu-id="0a8f5-170">URL-адрес страницы с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-170">The more information Url.</span></span> <span data-ttu-id="0a8f5-171">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-171">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-172">owner</span><span class="sxs-lookup"><span data-stu-id="0a8f5-172">owner</span></span>|<span data-ttu-id="0a8f5-173">String</span><span class="sxs-lookup"><span data-stu-id="0a8f5-173">String</span></span>|<span data-ttu-id="0a8f5-174">Владелец приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-174">The owner of the app.</span></span> <span data-ttu-id="0a8f5-175">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-175">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-176">developer</span><span class="sxs-lookup"><span data-stu-id="0a8f5-176">developer</span></span>|<span data-ttu-id="0a8f5-177">String</span><span class="sxs-lookup"><span data-stu-id="0a8f5-177">String</span></span>|<span data-ttu-id="0a8f5-178">Разработчик приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-178">The developer of the app.</span></span> <span data-ttu-id="0a8f5-179">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-179">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-180">notes</span><span class="sxs-lookup"><span data-stu-id="0a8f5-180">notes</span></span>|<span data-ttu-id="0a8f5-181">String</span><span class="sxs-lookup"><span data-stu-id="0a8f5-181">String</span></span>|<span data-ttu-id="0a8f5-182">Заметки для приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-182">Notes for the app.</span></span> <span data-ttu-id="0a8f5-183">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-183">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="0a8f5-184">uploadState</span></span>|<span data-ttu-id="0a8f5-185">Int32</span><span class="sxs-lookup"><span data-stu-id="0a8f5-185">Int32</span></span>|<span data-ttu-id="0a8f5-186">Состояние отправки.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-186">The upload state.</span></span> <span data-ttu-id="0a8f5-187">Возможные значения: 0 – `Not Ready` , 1 – `Ready` , 2 `Processing` .</span><span class="sxs-lookup"><span data-stu-id="0a8f5-187">Possible values are: 0 - `Not Ready`, 1 - `Ready`, 2 - `Processing`.</span></span> <span data-ttu-id="0a8f5-188">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-188">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-189">publishingState</span><span class="sxs-lookup"><span data-stu-id="0a8f5-189">publishingState</span></span>|[<span data-ttu-id="0a8f5-190">мобилеапппублишингстате</span><span class="sxs-lookup"><span data-stu-id="0a8f5-190">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="0a8f5-191">Состояние публикации для приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-191">The publishing state for the app.</span></span> <span data-ttu-id="0a8f5-192">Приложение невозможно назначить, если оно не опубликовано.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-192">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="0a8f5-193">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-193">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md).</span></span> <span data-ttu-id="0a8f5-194">Возможные значения: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-194">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="0a8f5-195">isAssigned</span><span class="sxs-lookup"><span data-stu-id="0a8f5-195">isAssigned</span></span>|<span data-ttu-id="0a8f5-196">Boolean</span><span class="sxs-lookup"><span data-stu-id="0a8f5-196">Boolean</span></span>|<span data-ttu-id="0a8f5-197">Значение, указывающее, назначено ли приложение по крайней мере одной группе.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-197">The value indicating whether the app is assigned to at least one group.</span></span> <span data-ttu-id="0a8f5-198">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-198">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-199">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="0a8f5-199">roleScopeTagIds</span></span>|<span data-ttu-id="0a8f5-200">Коллекция String</span><span class="sxs-lookup"><span data-stu-id="0a8f5-200">String collection</span></span>|<span data-ttu-id="0a8f5-201">Список идентификаторов тегов области для этого мобильного приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-201">List of scope tag ids for this mobile app.</span></span> <span data-ttu-id="0a8f5-202">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-202">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-203">депендентаппкаунт</span><span class="sxs-lookup"><span data-stu-id="0a8f5-203">dependentAppCount</span></span>|<span data-ttu-id="0a8f5-204">Int32</span><span class="sxs-lookup"><span data-stu-id="0a8f5-204">Int32</span></span>|<span data-ttu-id="0a8f5-205">Общее количество зависимостей для дочернего приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-205">The total number of dependencies the child app has.</span></span> <span data-ttu-id="0a8f5-206">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-206">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-207">суперседингаппкаунт</span><span class="sxs-lookup"><span data-stu-id="0a8f5-207">supersedingAppCount</span></span>|<span data-ttu-id="0a8f5-208">Int32</span><span class="sxs-lookup"><span data-stu-id="0a8f5-208">Int32</span></span>|<span data-ttu-id="0a8f5-209">Общее количество приложений, которые напрямую или косвенно заменяют данное приложение.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-209">The total number of apps this app directly or indirectly supersedes.</span></span> <span data-ttu-id="0a8f5-210">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-210">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|
|<span data-ttu-id="0a8f5-211">суперседедаппкаунт</span><span class="sxs-lookup"><span data-stu-id="0a8f5-211">supersededAppCount</span></span>|<span data-ttu-id="0a8f5-212">Int32</span><span class="sxs-lookup"><span data-stu-id="0a8f5-212">Int32</span></span>|<span data-ttu-id="0a8f5-213">Общее число приложений, для которых это приложение напрямую или косвенно заменяется.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-213">The total number of apps this app is directly or indirectly superseded by.</span></span> <span data-ttu-id="0a8f5-214">Наследуется от [mobileApp](../resources/intune-shared-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f5-214">Inherited from [mobileApp](../resources/intune-shared-mobileapp.md)</span></span>|



## <a name="response"></a><span data-ttu-id="0a8f5-215">Отклик</span><span class="sxs-lookup"><span data-stu-id="0a8f5-215">Response</span></span>
<span data-ttu-id="0a8f5-216">В случае успешного выполнения этот метод возвращает код отклика `200 OK` и обновленный объект [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-216">If successful, this method returns a `200 OK` response code and an updated [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0a8f5-217">Пример</span><span class="sxs-lookup"><span data-stu-id="0a8f5-217">Example</span></span>

### <a name="request"></a><span data-ttu-id="0a8f5-218">Запрос</span><span class="sxs-lookup"><span data-stu-id="0a8f5-218">Request</span></span>
<span data-ttu-id="0a8f5-219">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-219">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 775

{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
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
  "supersededAppCount": 2
}
```

### <a name="response"></a><span data-ttu-id="0a8f5-220">Отклик</span><span class="sxs-lookup"><span data-stu-id="0a8f5-220">Response</span></span>
<span data-ttu-id="0a8f5-p121">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="0a8f5-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 947

{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
  "id": "bf39e35d-e35d-bf39-5de3-39bf5de339bf",
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
  "supersededAppCount": 2
}
```






