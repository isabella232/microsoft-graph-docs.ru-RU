---
title: Обновление Андроидворкпрофилекустомконфигуратион
description: Обновление свойств объекта Андроидворкпрофилекустомконфигуратион.
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: 89b50faeffbea78c816763a21a6bc1cd55c78427
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2019
ms.locfileid: "34969507"
---
# <a name="update-androidworkprofilecustomconfiguration"></a><span data-ttu-id="75c6c-103">Обновление Андроидворкпрофилекустомконфигуратион</span><span class="sxs-lookup"><span data-stu-id="75c6c-103">Update androidWorkProfileCustomConfiguration</span></span>

> <span data-ttu-id="75c6c-104">**Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="75c6c-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="75c6c-105">**Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="75c6c-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="75c6c-106">Обновление свойств объекта [андроидворкпрофилекустомконфигуратион](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="75c6c-106">Update the properties of a [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="75c6c-107">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="75c6c-107">Prerequisites</span></span>
<span data-ttu-id="75c6c-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="75c6c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="75c6c-110">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="75c6c-110">Permission type</span></span>|<span data-ttu-id="75c6c-111">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="75c6c-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="75c6c-112">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="75c6c-112">Delegated (work or school account)</span></span>|<span data-ttu-id="75c6c-113">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="75c6c-113">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="75c6c-114">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="75c6c-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="75c6c-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="75c6c-115">Not supported.</span></span>|
|<span data-ttu-id="75c6c-116">Для приложений</span><span class="sxs-lookup"><span data-stu-id="75c6c-116">Application</span></span>|<span data-ttu-id="75c6c-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="75c6c-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="75c6c-118">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="75c6c-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="75c6c-119">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="75c6c-119">Request headers</span></span>
|<span data-ttu-id="75c6c-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="75c6c-120">Header</span></span>|<span data-ttu-id="75c6c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="75c6c-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="75c6c-122">Авторизация</span><span class="sxs-lookup"><span data-stu-id="75c6c-122">Authorization</span></span>|<span data-ttu-id="75c6c-123">Bearer &lt;token&gt;. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="75c6c-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="75c6c-124">Accept</span><span class="sxs-lookup"><span data-stu-id="75c6c-124">Accept</span></span>|<span data-ttu-id="75c6c-125">application/json</span><span class="sxs-lookup"><span data-stu-id="75c6c-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="75c6c-126">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="75c6c-126">Request body</span></span>
<span data-ttu-id="75c6c-127">В тексте запроса добавьте представление объекта [андроидворкпрофилекустомконфигуратион](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="75c6c-127">In the request body, supply a JSON representation for the [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object.</span></span>

<span data-ttu-id="75c6c-128">В следующей таблице приведены свойства, необходимые при создании [андроидворкпрофилекустомконфигуратион](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="75c6c-128">The following table shows the properties that are required when you create the [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md).</span></span>

|<span data-ttu-id="75c6c-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="75c6c-129">Property</span></span>|<span data-ttu-id="75c6c-130">Тип</span><span class="sxs-lookup"><span data-stu-id="75c6c-130">Type</span></span>|<span data-ttu-id="75c6c-131">Описание</span><span class="sxs-lookup"><span data-stu-id="75c6c-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75c6c-132">id</span><span class="sxs-lookup"><span data-stu-id="75c6c-132">id</span></span>|<span data-ttu-id="75c6c-133">String</span><span class="sxs-lookup"><span data-stu-id="75c6c-133">String</span></span>|<span data-ttu-id="75c6c-134">Ключ объекта.</span><span class="sxs-lookup"><span data-stu-id="75c6c-134">Key of the entity.</span></span> <span data-ttu-id="75c6c-135">Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="75c6c-135">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="75c6c-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="75c6c-136">lastModifiedDateTime</span></span>|<span data-ttu-id="75c6c-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="75c6c-137">DateTimeOffset</span></span>|<span data-ttu-id="75c6c-138">Дата и время последнего изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="75c6c-138">DateTime the object was last modified.</span></span> <span data-ttu-id="75c6c-139">Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="75c6c-139">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="75c6c-140">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="75c6c-140">roleScopeTagIds</span></span>|<span data-ttu-id="75c6c-141">Коллекция строк</span><span class="sxs-lookup"><span data-stu-id="75c6c-141">String collection</span></span>|<span data-ttu-id="75c6c-142">Список тегов областей для этого экземпляра сущности.</span><span class="sxs-lookup"><span data-stu-id="75c6c-142">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="75c6c-143">Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="75c6c-143">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="75c6c-144">Суппортсскопетагс</span><span class="sxs-lookup"><span data-stu-id="75c6c-144">supportsScopeTags</span></span>|<span data-ttu-id="75c6c-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="75c6c-145">Boolean</span></span>|<span data-ttu-id="75c6c-146">Указывает, поддерживает ли базовая конфигурация устройства назначение тегов области.</span><span class="sxs-lookup"><span data-stu-id="75c6c-146">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="75c6c-147">Назначение свойства Скопетагс не разрешено, если это значение равно false, а сущности не будут отображаться для пользователей с ограниченной областью действия.</span><span class="sxs-lookup"><span data-stu-id="75c6c-147">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="75c6c-148">Это происходит для устаревших политик, созданных в Silverlight, и может быть разрешено путем удаления и повторного создания политики на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="75c6c-148">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="75c6c-149">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="75c6c-149">This property is read-only.</span></span> <span data-ttu-id="75c6c-150">Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="75c6c-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="75c6c-151">deviceManagementApplicabilityRuleOsEdition</span><span class="sxs-lookup"><span data-stu-id="75c6c-151">deviceManagementApplicabilityRuleOsEdition</span></span>|[<span data-ttu-id="75c6c-152">deviceManagementApplicabilityRuleOsEdition</span><span class="sxs-lookup"><span data-stu-id="75c6c-152">deviceManagementApplicabilityRuleOsEdition</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosedition.md)|<span data-ttu-id="75c6c-153">Применимость выпусков ОС для этой политики.</span><span class="sxs-lookup"><span data-stu-id="75c6c-153">The OS edition applicability for this Policy.</span></span> <span data-ttu-id="75c6c-154">Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="75c6c-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="75c6c-155">deviceManagementApplicabilityRuleOsVersion</span><span class="sxs-lookup"><span data-stu-id="75c6c-155">deviceManagementApplicabilityRuleOsVersion</span></span>|[<span data-ttu-id="75c6c-156">deviceManagementApplicabilityRuleOsVersion</span><span class="sxs-lookup"><span data-stu-id="75c6c-156">deviceManagementApplicabilityRuleOsVersion</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosversion.md)|<span data-ttu-id="75c6c-157">Правило применимости версии ОС для этой политики.</span><span class="sxs-lookup"><span data-stu-id="75c6c-157">The OS version applicability rule for this Policy.</span></span> <span data-ttu-id="75c6c-158">Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="75c6c-158">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="75c6c-159">Девицеманажементаппликабилитируледевицемоде</span><span class="sxs-lookup"><span data-stu-id="75c6c-159">deviceManagementApplicabilityRuleDeviceMode</span></span>|[<span data-ttu-id="75c6c-160">Девицеманажементаппликабилитируледевицемоде</span><span class="sxs-lookup"><span data-stu-id="75c6c-160">deviceManagementApplicabilityRuleDeviceMode</span></span>](../resources/intune-deviceconfig-devicemanagementapplicabilityruledevicemode.md)|<span data-ttu-id="75c6c-161">Правило применимости режима устройства для этой политики.</span><span class="sxs-lookup"><span data-stu-id="75c6c-161">The device mode applicability rule for this Policy.</span></span> <span data-ttu-id="75c6c-162">Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="75c6c-162">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="75c6c-163">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="75c6c-163">createdDateTime</span></span>|<span data-ttu-id="75c6c-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="75c6c-164">DateTimeOffset</span></span>|<span data-ttu-id="75c6c-165">Дата и время создания объекта.</span><span class="sxs-lookup"><span data-stu-id="75c6c-165">DateTime the object was created.</span></span> <span data-ttu-id="75c6c-166">Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="75c6c-166">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="75c6c-167">description</span><span class="sxs-lookup"><span data-stu-id="75c6c-167">description</span></span>|<span data-ttu-id="75c6c-168">String</span><span class="sxs-lookup"><span data-stu-id="75c6c-168">String</span></span>|<span data-ttu-id="75c6c-169">Указанное администратором описание конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="75c6c-169">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="75c6c-170">Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="75c6c-170">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="75c6c-171">displayName</span><span class="sxs-lookup"><span data-stu-id="75c6c-171">displayName</span></span>|<span data-ttu-id="75c6c-172">Строка</span><span class="sxs-lookup"><span data-stu-id="75c6c-172">String</span></span>|<span data-ttu-id="75c6c-173">Указанное администратором имя конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="75c6c-173">Admin provided name of the device configuration.</span></span> <span data-ttu-id="75c6c-174">Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="75c6c-174">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="75c6c-175">version</span><span class="sxs-lookup"><span data-stu-id="75c6c-175">version</span></span>|<span data-ttu-id="75c6c-176">Int32</span><span class="sxs-lookup"><span data-stu-id="75c6c-176">Int32</span></span>|<span data-ttu-id="75c6c-177">Версия конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="75c6c-177">Version of the device configuration.</span></span> <span data-ttu-id="75c6c-178">Наследуется от объекта [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="75c6c-178">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="75c6c-179">omaSettings</span><span class="sxs-lookup"><span data-stu-id="75c6c-179">omaSettings</span></span>|<span data-ttu-id="75c6c-180">Коллекция [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="75c6c-180">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="75c6c-181">Параметры OMA.</span><span class="sxs-lookup"><span data-stu-id="75c6c-181">OMA settings.</span></span> <span data-ttu-id="75c6c-182">Эта коллекция может содержать не более 500 элементов.</span><span class="sxs-lookup"><span data-stu-id="75c6c-182">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="75c6c-183">Ответ</span><span class="sxs-lookup"><span data-stu-id="75c6c-183">Response</span></span>
<span data-ttu-id="75c6c-184">В случае успешного выполнения этот метод возвращает `200 OK` код отклика и обновленный объект [андроидворкпрофилекустомконфигуратион](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="75c6c-184">If successful, this method returns a `200 OK` response code and an updated [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="75c6c-185">Пример</span><span class="sxs-lookup"><span data-stu-id="75c6c-185">Example</span></span>

### <a name="request"></a><span data-ttu-id="75c6c-186">Запрос</span><span class="sxs-lookup"><span data-stu-id="75c6c-186">Request</span></span>
<span data-ttu-id="75c6c-187">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="75c6c-187">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1305

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCustomConfiguration",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "deviceManagementApplicabilityRuleOsEdition": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsEdition",
    "osEditionTypes": [
      "windows10EnterpriseN"
    ],
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleOsVersion": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsVersion",
    "minOSVersion": "Min OSVersion value",
    "maxOSVersion": "Max OSVersion value",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleDeviceMode": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleDeviceMode",
    "deviceMode": "sModeConfiguration",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSettingInteger",
      "displayName": "Display Name value",
      "description": "Description value",
      "omaUri": "Oma Uri value",
      "value": 5,
      "isReadOnly": true
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="75c6c-188">Отклик</span><span class="sxs-lookup"><span data-stu-id="75c6c-188">Response</span></span>
<span data-ttu-id="75c6c-p114">Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="75c6c-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1477

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCustomConfiguration",
  "id": "76c5d59b-d59b-76c5-9bd5-c5769bd5c576",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "deviceManagementApplicabilityRuleOsEdition": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsEdition",
    "osEditionTypes": [
      "windows10EnterpriseN"
    ],
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleOsVersion": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsVersion",
    "minOSVersion": "Min OSVersion value",
    "maxOSVersion": "Max OSVersion value",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "deviceManagementApplicabilityRuleDeviceMode": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleDeviceMode",
    "deviceMode": "sModeConfiguration",
    "name": "Name value",
    "ruleType": "exclude"
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSettingInteger",
      "displayName": "Display Name value",
      "description": "Description value",
      "omaUri": "Oma Uri value",
      "value": 5,
      "isReadOnly": true
    }
  ]
}
```





