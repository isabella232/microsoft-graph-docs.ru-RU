---
title: Обновление объекта deviceConfigurationUserOverview
description: Обновление свойств объекта deviceConfigurationUserOverview.
author: tfitzmac
ms.openlocfilehash: 9aac0cc7c578ed281999391f4db88e29ee336cfc
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311468"
---
# <a name="update-deviceconfigurationuseroverview"></a><span data-ttu-id="06916-103">Обновление объекта deviceConfigurationUserOverview</span><span class="sxs-lookup"><span data-stu-id="06916-103">Update deviceConfigurationUserOverview</span></span>

> <span data-ttu-id="06916-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="06916-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="06916-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="06916-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="06916-106">**Примечание.** Для настройки элементов управления и политик Intune с помощью API Microsoft Graph по-прежнему требуется, чтобы клиент [лицензировал](https://go.microsoft.com/fwlink/?linkid=839381) Intune надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="06916-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="06916-107">Обновление свойств объекта [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="06916-107">Update the properties of a [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="06916-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="06916-108">Prerequisites</span></span>
<span data-ttu-id="06916-p102">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="06916-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="06916-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="06916-111">Permission type</span></span>|<span data-ttu-id="06916-112">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="06916-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="06916-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="06916-113">Delegated (work or school account)</span></span>|<span data-ttu-id="06916-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="06916-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="06916-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="06916-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="06916-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="06916-116">Not supported.</span></span>|
|<span data-ttu-id="06916-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="06916-117">Application</span></span>|<span data-ttu-id="06916-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="06916-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="06916-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="06916-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatusOverview
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/userStatusOverview
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/userStatusOverview
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/userStatusOverview
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/userStatusOverview
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/userStatusOverview
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/userStatusOverview
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/userStatusOverview
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/userStatusOverview
```

## <a name="request-headers"></a><span data-ttu-id="06916-120">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="06916-120">Request headers</span></span>
|<span data-ttu-id="06916-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="06916-121">Header</span></span>|<span data-ttu-id="06916-122">Значение</span><span class="sxs-lookup"><span data-stu-id="06916-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="06916-123">Авторизация</span><span class="sxs-lookup"><span data-stu-id="06916-123">Authorization</span></span>|<span data-ttu-id="06916-124">Требуется Bearer &lt;маркер&gt;
</span><span class="sxs-lookup"><span data-stu-id="06916-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="06916-125">Accept</span><span class="sxs-lookup"><span data-stu-id="06916-125">Accept</span></span>|<span data-ttu-id="06916-126">application/json</span><span class="sxs-lookup"><span data-stu-id="06916-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="06916-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="06916-127">Request body</span></span>
<span data-ttu-id="06916-128">В тексте запроса добавьте представление объекта [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="06916-128">In the request body, supply a JSON representation for the [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md) object.</span></span>

<span data-ttu-id="06916-129">В таблице ниже приведены свойства, которые необходимо указывать при создании объекта [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="06916-129">The following table shows the properties that are required when you create the [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md).</span></span>

|<span data-ttu-id="06916-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="06916-130">Property</span></span>|<span data-ttu-id="06916-131">Тип</span><span class="sxs-lookup"><span data-stu-id="06916-131">Type</span></span>|<span data-ttu-id="06916-132">Описание</span><span class="sxs-lookup"><span data-stu-id="06916-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="06916-133">id</span><span class="sxs-lookup"><span data-stu-id="06916-133">id</span></span>|<span data-ttu-id="06916-134">Строка</span><span class="sxs-lookup"><span data-stu-id="06916-134">String</span></span>|<span data-ttu-id="06916-135">Ключ объекта.</span><span class="sxs-lookup"><span data-stu-id="06916-135">Key of the entity.</span></span>|
|<span data-ttu-id="06916-136">pendingCount</span><span class="sxs-lookup"><span data-stu-id="06916-136">pendingCount</span></span>|<span data-ttu-id="06916-137">Int32</span><span class="sxs-lookup"><span data-stu-id="06916-137">Int32</span></span>|<span data-ttu-id="06916-138">Количество ожидающих пользователей.</span><span class="sxs-lookup"><span data-stu-id="06916-138">Number of pending Users</span></span>|
|<span data-ttu-id="06916-139">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="06916-139">notApplicableCount</span></span>|<span data-ttu-id="06916-140">Int32</span><span class="sxs-lookup"><span data-stu-id="06916-140">Int32</span></span>|<span data-ttu-id="06916-141">Число пользователей не применим</span><span class="sxs-lookup"><span data-stu-id="06916-141">Number of not applicable users</span></span>|
|<span data-ttu-id="06916-142">successCount</span><span class="sxs-lookup"><span data-stu-id="06916-142">successCount</span></span>|<span data-ttu-id="06916-143">Int32</span><span class="sxs-lookup"><span data-stu-id="06916-143">Int32</span></span>|<span data-ttu-id="06916-144">Количество успешных пользователей.</span><span class="sxs-lookup"><span data-stu-id="06916-144">Number of succeeded Users</span></span>|
|<span data-ttu-id="06916-145">errorCount</span><span class="sxs-lookup"><span data-stu-id="06916-145">errorCount</span></span>|<span data-ttu-id="06916-146">Int32</span><span class="sxs-lookup"><span data-stu-id="06916-146">Int32</span></span>|<span data-ttu-id="06916-147">Количество пользователей с ошибками.</span><span class="sxs-lookup"><span data-stu-id="06916-147">Number of error Users</span></span>|
|<span data-ttu-id="06916-148">failedCount</span><span class="sxs-lookup"><span data-stu-id="06916-148">failedCount</span></span>|<span data-ttu-id="06916-149">Int32</span><span class="sxs-lookup"><span data-stu-id="06916-149">Int32</span></span>|<span data-ttu-id="06916-150">Количество пользователей со сбоями.</span><span class="sxs-lookup"><span data-stu-id="06916-150">Number of failed Users</span></span>|
|<span data-ttu-id="06916-151">conflictCount</span><span class="sxs-lookup"><span data-stu-id="06916-151">conflictCount</span></span>|<span data-ttu-id="06916-152">Int32</span><span class="sxs-lookup"><span data-stu-id="06916-152">Int32</span></span>|<span data-ttu-id="06916-153">Количество пользователей в конфликта</span><span class="sxs-lookup"><span data-stu-id="06916-153">Number of users in conflict</span></span>|
|<span data-ttu-id="06916-154">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="06916-154">lastUpdateDateTime</span></span>|<span data-ttu-id="06916-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="06916-155">DateTimeOffset</span></span>|<span data-ttu-id="06916-156">Время последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="06916-156">Last update time</span></span>|
|<span data-ttu-id="06916-157">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="06916-157">configurationVersion</span></span>|<span data-ttu-id="06916-158">Int32</span><span class="sxs-lookup"><span data-stu-id="06916-158">Int32</span></span>|<span data-ttu-id="06916-159">Версия политики для этого обзора.</span><span class="sxs-lookup"><span data-stu-id="06916-159">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="06916-160">Отклик</span><span class="sxs-lookup"><span data-stu-id="06916-160">Response</span></span>
<span data-ttu-id="06916-161">В случае успешного выполнения этот метод возвращает код отклика `200 OK` и обновленный объект [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="06916-161">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="06916-162">Пример</span><span class="sxs-lookup"><span data-stu-id="06916-162">Example</span></span>
### <a name="request"></a><span data-ttu-id="06916-163">Запрос</span><span class="sxs-lookup"><span data-stu-id="06916-163">Request</span></span>
<span data-ttu-id="06916-164">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="06916-164">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatusOverview
Content-type: application/json
Content-length: 236

{
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "conflictCount": 13,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```

### <a name="response"></a><span data-ttu-id="06916-165">Ответ</span><span class="sxs-lookup"><span data-stu-id="06916-165">Response</span></span>
<span data-ttu-id="06916-p103">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="06916-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 355

{
  "@odata.type": "#microsoft.graph.deviceConfigurationUserOverview",
  "id": "000e52d7-52d7-000e-d752-0e00d7520e00",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "conflictCount": 13,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```





