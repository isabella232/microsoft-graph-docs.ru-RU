---
title: Создание Команажементелигибледевице
description: Создание нового объекта Команажементелигибледевице.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: 3a852c653a0a4ca57411514aa0ebd66bfb362500
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49229487"
---
# <a name="create-comanagementeligibledevice"></a>Создание Команажементелигибледевице

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Создание нового объекта [команажементелигибледевице](../resources/intune-devices-comanagementeligibledevice.md) .

## <a name="prerequisites"></a>Необходимые компоненты
Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

|Тип разрешения|Разрешения (в порядке убывания привилегий)|
|:---|:---|
|Делегированные (рабочая или учебная учетная запись)|DeviceManagementManagedDevices.ReadWrite.All|
|Делегированные (личная учетная запись Майкрософт)|Не поддерживается.|
|Приложение|DeviceManagementManagedDevices.ReadWrite.All|

## <a name="http-request"></a>HTTP-запрос
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/comanagementEligibleDevices
```

## <a name="request-headers"></a>Заголовки запроса
|Заголовок|Значение|
|:---|:---|
|Авторизация|Bearer &lt;token&gt;. Обязательный.|
|Accept|application/json|

## <a name="request-body"></a>Текст запроса
В тексте запроса добавьте представление объекта Команажементелигибледевице в формате JSON.

В следующей таблице приведены свойства, необходимые при создании Команажементелигибледевице.

|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Уникальный идентификатор устройства|
|deviceName|String|DeviceName|
|deviceType|[deviceType](../resources/intune-shared-devicetype.md)|DeviceType. Возможные значения:,,,,,,,,,,, `desktop` `windowsRT` `winMO6` `nokia` `windowsPhone` `mac` `winCE` `winEmbedded` `iPhone` `iPad` `iPod` `android` `iSocConsumer` , `unix` ,,, `macMDM` `holoLens` `surfaceHub` `androidForWork` `androidEnterprise` `windows10x` `androidnGMS` `blackberry` `palm` `unknown` ,, `cloudPC` ,,,,,,,,,,,,,.|
|клиентрегистратионстатус|[deviceRegistrationState](../resources/intune-devices-deviceregistrationstate.md)|Клиентрегистратионстатус. Возможные значения: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment`, `unknown`.|
|ownerType|[ownerType](../resources/intune-shared-ownertype.md)|OwnerType. Возможные значения: `unknown`, `company`, `personal`.|
|managementAgents|[манажементаженттипе](../resources/intune-shared-managementagenttype.md)|ManagementAgents. Возможные значения: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`, `microsoft365ManagedMdm`.|
|манажементстате|[манажементстате](../resources/intune-devices-managementstate.md)|Манажементстате. Возможные значения: `managed`, `retirePending`, `retireFailed`, `wipePending`, `wipeFailed`, `unhealthy`, `deletePending`, `retireIssued`, `wipeIssued`, `wipeCanceled`, `retireCanceled`, `discovered`.|
|референцеид|String|ReferenceId|
|мдмстатус|String|мдмстатус|
|osVersion|String|OSVersion|
|serialNumber|String|SerialNumber|
|manufacturer|String|Вычислитель|
|model|String|Модель|
|osDescription|String|Свойства OSDescription|
|ентитисаурце|Int32|ентитисаурце|
|userId|String|ИД пользователя|
|Основное|String|UPN|
|userEmail|String|Электронный адрес пользователя|
|userName|String|Имя пользователя|
|status|[comanagementEligibleType](../resources/intune-devices-comanagementeligibletype.md)|Команажементелигиблестатус. Возможные значения: `comanaged`, `eligible`, `eligibleButNotAzureAdJoined`, `needsOsUpdate`, `ineligible`.|



## <a name="response"></a>Отклик
В случае успешного выполнения этот метод возвращает `201 Created` код отклика и объект [команажементелигибледевице](../resources/intune-devices-comanagementeligibledevice.md) в тексте отклика.

## <a name="example"></a>Пример

### <a name="request"></a>Запрос
Ниже приведен пример запроса.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/comanagementEligibleDevices
Content-type: application/json
Content-length: 714

{
  "@odata.type": "#microsoft.graph.comanagementEligibleDevice",
  "deviceName": "Device Name value",
  "deviceType": "windowsRT",
  "clientRegistrationStatus": "registered",
  "ownerType": "company",
  "managementAgents": "mdm",
  "managementState": "retirePending",
  "referenceId": "Reference Id value",
  "mdmStatus": "Mdm Status value",
  "osVersion": "Os Version value",
  "serialNumber": "Serial Number value",
  "manufacturer": "Manufacturer value",
  "model": "Model value",
  "osDescription": "Os Description value",
  "entitySource": 12,
  "userId": "User Id value",
  "upn": "Upn value",
  "userEmail": "User Email value",
  "userName": "User Name value",
  "status": "eligible"
}
```

### <a name="response"></a>Отклик
Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 763

{
  "@odata.type": "#microsoft.graph.comanagementEligibleDevice",
  "id": "ac20683b-683b-ac20-3b68-20ac3b6820ac",
  "deviceName": "Device Name value",
  "deviceType": "windowsRT",
  "clientRegistrationStatus": "registered",
  "ownerType": "company",
  "managementAgents": "mdm",
  "managementState": "retirePending",
  "referenceId": "Reference Id value",
  "mdmStatus": "Mdm Status value",
  "osVersion": "Os Version value",
  "serialNumber": "Serial Number value",
  "manufacturer": "Manufacturer value",
  "model": "Model value",
  "osDescription": "Os Description value",
  "entitySource": 12,
  "userId": "User Id value",
  "upn": "Upn value",
  "userEmail": "User Email value",
  "userName": "User Name value",
  "status": "eligible"
}
```




