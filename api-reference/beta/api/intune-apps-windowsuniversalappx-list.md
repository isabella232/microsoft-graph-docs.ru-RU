---
title: Перечисление объектов windowsUniversalAppX
description: Список свойств и связей объектов windowsUniversalAppX.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 2a566f365c3acb616d163283e11d16ad1faebdbc
ms.sourcegitcommit: 53dd31d323319fbd2ff7afc51b55a46efb8c5be3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2019
ms.locfileid: "39932469"
---
# <a name="list-windowsuniversalappxs"></a><span data-ttu-id="a9788-103">Перечисление объектов windowsUniversalAppX</span><span class="sxs-lookup"><span data-stu-id="a9788-103">List windowsUniversalAppXs</span></span>

> <span data-ttu-id="a9788-104">**Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9788-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="a9788-105">**Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="a9788-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="a9788-106">Список свойств и связей объектов [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="a9788-106">List properties and relationships of the [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a9788-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="a9788-107">Prerequisites</span></span>
<span data-ttu-id="a9788-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a9788-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a9788-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="a9788-110">Permission type</span></span>|<span data-ttu-id="a9788-111">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="a9788-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a9788-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a9788-112">Delegated (work or school account)</span></span>|<span data-ttu-id="a9788-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="a9788-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="a9788-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="a9788-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a9788-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9788-115">Not supported.</span></span>|
|<span data-ttu-id="a9788-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="a9788-116">Application</span></span>|<span data-ttu-id="a9788-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="a9788-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|

## <a name="http-request"></a><span data-ttu-id="a9788-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="a9788-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="a9788-119">Заголовки запроса</span><span class="sxs-lookup"><span data-stu-id="a9788-119">Request headers</span></span>
|<span data-ttu-id="a9788-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a9788-120">Header</span></span>|<span data-ttu-id="a9788-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a9788-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a9788-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="a9788-122">Authorization</span></span>|<span data-ttu-id="a9788-123">Bearer &lt;token&gt;. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a9788-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a9788-124">Accept</span><span class="sxs-lookup"><span data-stu-id="a9788-124">Accept</span></span>|<span data-ttu-id="a9788-125">application/json</span><span class="sxs-lookup"><span data-stu-id="a9788-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a9788-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="a9788-126">Request body</span></span>
<span data-ttu-id="a9788-127">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="a9788-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a9788-128">Ответ</span><span class="sxs-lookup"><span data-stu-id="a9788-128">Response</span></span>
<span data-ttu-id="a9788-129">При успешном выполнении этот метод возвращает код отклика `200 OK` и коллекцию объектов [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="a9788-129">If successful, this method returns a `200 OK` response code and a collection of [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a9788-130">Пример</span><span class="sxs-lookup"><span data-stu-id="a9788-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="a9788-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="a9788-131">Request</span></span>
<span data-ttu-id="a9788-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="a9788-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="a9788-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="a9788-133">Response</span></span>
<span data-ttu-id="a9788-p102">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="a9788-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1854

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsUniversalAppX",
      "id": "4bc47eba-7eba-4bc4-ba7e-c44bba7ec44b",
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
      "applicableArchitectures": "x86",
      "applicableDeviceTypes": "desktop",
      "identityName": "Identity Name value",
      "identityPublisherHash": "Identity Publisher Hash value",
      "identityResourceIdentifier": "Identity Resource Identifier value",
      "isBundle": true,
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
      "identityVersion": "Identity Version value"
    }
  ]
}
```





