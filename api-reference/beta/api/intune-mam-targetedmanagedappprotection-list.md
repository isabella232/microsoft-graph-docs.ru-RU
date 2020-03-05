---
title: Перечисление объектов targetedManagedAppProtection
description: Перечисление свойств и связей объектов targetedManagedAppProtection.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 1a68a817e3c2925b4315c64048e177ae6255af75
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42463162"
---
# <a name="list-targetedmanagedappprotections"></a><span data-ttu-id="57f18-103">Перечисление объектов targetedManagedAppProtection</span><span class="sxs-lookup"><span data-stu-id="57f18-103">List targetedManagedAppProtections</span></span>

<span data-ttu-id="57f18-104">Пространство имен: Microsoft. Graph</span><span class="sxs-lookup"><span data-stu-id="57f18-104">Namespace: microsoft.graph</span></span>

> <span data-ttu-id="57f18-105">**Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="57f18-105">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="57f18-106">**Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="57f18-106">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="57f18-107">Перечисление свойств и связей объектов [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="57f18-107">List properties and relationships of the [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="57f18-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="57f18-108">Prerequisites</span></span>
<span data-ttu-id="57f18-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="57f18-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="57f18-111">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="57f18-111">Permission type</span></span>|<span data-ttu-id="57f18-112">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="57f18-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="57f18-113">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="57f18-113">Delegated (work or school account)</span></span>|<span data-ttu-id="57f18-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="57f18-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="57f18-115">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="57f18-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="57f18-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="57f18-116">Not supported.</span></span>|
|<span data-ttu-id="57f18-117">Для приложений</span><span class="sxs-lookup"><span data-stu-id="57f18-117">Application</span></span>|<span data-ttu-id="57f18-118">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="57f18-118">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="57f18-119">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="57f18-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies
```

## <a name="request-headers"></a><span data-ttu-id="57f18-120">Заголовки запроса</span><span class="sxs-lookup"><span data-stu-id="57f18-120">Request headers</span></span>
|<span data-ttu-id="57f18-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="57f18-121">Header</span></span>|<span data-ttu-id="57f18-122">Значение</span><span class="sxs-lookup"><span data-stu-id="57f18-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="57f18-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="57f18-123">Authorization</span></span>|<span data-ttu-id="57f18-124">Bearer &lt;token&gt;. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="57f18-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="57f18-125">Accept</span><span class="sxs-lookup"><span data-stu-id="57f18-125">Accept</span></span>|<span data-ttu-id="57f18-126">application/json</span><span class="sxs-lookup"><span data-stu-id="57f18-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="57f18-127">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="57f18-127">Request body</span></span>
<span data-ttu-id="57f18-128">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="57f18-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="57f18-129">Ответ</span><span class="sxs-lookup"><span data-stu-id="57f18-129">Response</span></span>
<span data-ttu-id="57f18-130">При успешном выполнении этот метод возвращает код отклика `200 OK` и коллекцию объектов [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="57f18-130">If successful, this method returns a `200 OK` response code and a collection of [targetedManagedAppProtection](../resources/intune-mam-targetedmanagedappprotection.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="57f18-131">Пример</span><span class="sxs-lookup"><span data-stu-id="57f18-131">Example</span></span>

### <a name="request"></a><span data-ttu-id="57f18-132">Запрос</span><span class="sxs-lookup"><span data-stu-id="57f18-132">Request</span></span>
<span data-ttu-id="57f18-133">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="57f18-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/managedAppPolicies
```

### <a name="response"></a><span data-ttu-id="57f18-134">Отклик</span><span class="sxs-lookup"><span data-stu-id="57f18-134">Response</span></span>
<span data-ttu-id="57f18-p102">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="57f18-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2675

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.targetedManagedAppProtection",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "id": "b6b92266-2266-b6b9-6622-b9b66622b9b6",
      "version": "Version value",
      "periodOfflineBeforeAccessCheck": "-PT17.1357909S",
      "periodOnlineBeforeAccessCheck": "PT35.0018757S",
      "allowedInboundDataTransferSources": "managedApps",
      "allowedOutboundDataTransferDestinations": "managedApps",
      "organizationalCredentialsRequired": true,
      "allowedOutboundClipboardSharingLevel": "managedAppsWithPasteIn",
      "dataBackupBlocked": true,
      "deviceComplianceRequired": true,
      "managedBrowserToOpenLinksRequired": true,
      "saveAsBlocked": true,
      "periodOfflineBeforeWipeIsEnforced": "-PT3M22.1587532S",
      "pinRequired": true,
      "maximumPinRetries": 1,
      "simplePinBlocked": true,
      "minimumPinLength": 0,
      "pinCharacterSet": "alphanumericAndSymbol",
      "periodBeforePinReset": "PT3M29.6631862S",
      "allowedDataStorageLocations": [
        "sharePoint"
      ],
      "contactSyncBlocked": true,
      "printBlocked": true,
      "fingerprintBlocked": true,
      "disableAppPinIfDevicePinIsSet": true,
      "minimumRequiredOsVersion": "Minimum Required Os Version value",
      "minimumWarningOsVersion": "Minimum Warning Os Version value",
      "minimumRequiredAppVersion": "Minimum Required App Version value",
      "minimumWarningAppVersion": "Minimum Warning App Version value",
      "minimumWipeOsVersion": "Minimum Wipe Os Version value",
      "minimumWipeAppVersion": "Minimum Wipe App Version value",
      "appActionIfDeviceComplianceRequired": "wipe",
      "appActionIfMaximumPinRetriesExceeded": "wipe",
      "pinRequiredInsteadOfBiometricTimeout": "-PT3M9.8396734S",
      "allowedOutboundClipboardSharingExceptionLength": 14,
      "notificationRestriction": "blockOrganizationalData",
      "previousPinBlockCount": 5,
      "managedBrowser": "microsoftEdge",
      "maximumAllowedDeviceThreatLevel": "secured",
      "mobileThreatDefenseRemediationAction": "wipe",
      "blockDataIngestionIntoOrganizationDocuments": true,
      "allowedDataIngestionLocations": [
        "sharePoint"
      ],
      "appActionIfUnableToAuthenticateUser": "wipe",
      "isAssigned": true,
      "targetedAppManagementLevels": "unmanaged"
    }
  ]
}
```





