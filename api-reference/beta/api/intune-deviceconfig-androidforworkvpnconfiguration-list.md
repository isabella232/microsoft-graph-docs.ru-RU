---
title: Список Андроидфорворквпнконфигуратионс
description: Список свойств и связей объектов androidForWorkVpnConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 41ce65c4acc129eb934454a09dc0733436d9105c
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32478002"
---
# <a name="list-androidforworkvpnconfigurations"></a><span data-ttu-id="63e06-103">Список Андроидфорворквпнконфигуратионс</span><span class="sxs-lookup"><span data-stu-id="63e06-103">List androidForWorkVpnConfigurations</span></span>

> <span data-ttu-id="63e06-104">**Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="63e06-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="63e06-105">**Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="63e06-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="63e06-106">Список свойств и связей объектов [androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="63e06-106">List properties and relationships of the [androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="63e06-107">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="63e06-107">Prerequisites</span></span>
<span data-ttu-id="63e06-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63e06-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63e06-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="63e06-110">Permission type</span></span>|<span data-ttu-id="63e06-111">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="63e06-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63e06-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="63e06-112">Delegated (work or school account)</span></span>|<span data-ttu-id="63e06-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="63e06-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="63e06-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="63e06-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63e06-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="63e06-115">Not supported.</span></span>|
|<span data-ttu-id="63e06-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="63e06-116">Application</span></span>|<span data-ttu-id="63e06-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="63e06-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="63e06-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="63e06-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="63e06-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="63e06-119">Request headers</span></span>
|<span data-ttu-id="63e06-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="63e06-120">Header</span></span>|<span data-ttu-id="63e06-121">Значение</span><span class="sxs-lookup"><span data-stu-id="63e06-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63e06-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="63e06-122">Authorization</span></span>|<span data-ttu-id="63e06-123">Bearer &lt;token&gt;. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="63e06-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="63e06-124">Accept</span><span class="sxs-lookup"><span data-stu-id="63e06-124">Accept</span></span>|<span data-ttu-id="63e06-125">application/json</span><span class="sxs-lookup"><span data-stu-id="63e06-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63e06-126">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="63e06-126">Request body</span></span>
<span data-ttu-id="63e06-127">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="63e06-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="63e06-128">Ответ</span><span class="sxs-lookup"><span data-stu-id="63e06-128">Response</span></span>
<span data-ttu-id="63e06-129">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и коллекцию объектов [androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="63e06-129">If successful, this method returns a `200 OK` response code and a collection of [androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63e06-130">Пример</span><span class="sxs-lookup"><span data-stu-id="63e06-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="63e06-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="63e06-131">Request</span></span>
<span data-ttu-id="63e06-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="63e06-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="63e06-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="63e06-133">Response</span></span>
<span data-ttu-id="63e06-p102">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="63e06-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1346

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidForWorkVpnConfiguration",
      "id": "2cf4c52c-c52c-2cf4-2cc5-f42c2cc5f42c",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "supportsScopeTags": true,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "connectionName": "Connection Name value",
      "connectionType": "pulseSecure",
      "role": "Role value",
      "realm": "Realm value",
      "servers": [
        {
          "@odata.type": "microsoft.graph.vpnServer",
          "description": "Description value",
          "address": "Address value",
          "isDefaultServer": true
        }
      ],
      "fingerprint": "Fingerprint value",
      "customData": [
        {
          "@odata.type": "microsoft.graph.keyValue",
          "key": "Key value",
          "value": "Value value"
        }
      ],
      "customKeyValueData": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ],
      "authenticationMethod": "usernameAndPassword"
    }
  ]
}
```





