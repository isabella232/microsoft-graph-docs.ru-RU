---
title: Тип ресурса Виндовсвифиентерприсиапконфигуратион
description: Эта сущность предоставляет описания объявляемых методов, свойств и связей, предоставляемых CSP WiFi.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: cc94b4b05c38d3939c83ecef729acd677aab8522
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49226638"
---
# <a name="windowswifienterpriseeapconfiguration-resource-type"></a>Тип ресурса Виндовсвифиентерприсиапконфигуратион

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Эта сущность предоставляет описания объявляемых методов, свойств и связей, предоставляемых CSP WiFi.


Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md)

## <a name="methods"></a>Методы
|Метод|Возвращаемый тип|Описание|
|:---|:---|:---|
|[Список Виндовсвифиентерприсиапконфигуратионс](../api/intune-deviceconfig-windowswifienterpriseeapconfiguration-list.md)|Коллекция [виндовсвифиентерприсиапконфигуратион](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md)|Список свойств и связей объектов [виндовсвифиентерприсиапконфигуратион](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md) .|
|[Получение Виндовсвифиентерприсиапконфигуратион](../api/intune-deviceconfig-windowswifienterpriseeapconfiguration-get.md)|[виндовсвифиентерприсиапконфигуратион](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md)|Чтение свойств и связей объекта [виндовсвифиентерприсиапконфигуратион](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md) .|
|[Создание Виндовсвифиентерприсиапконфигуратион](../api/intune-deviceconfig-windowswifienterpriseeapconfiguration-create.md)|[виндовсвифиентерприсиапконфигуратион](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md)|Создание нового объекта [виндовсвифиентерприсиапконфигуратион](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md) .|
|[Удаление Виндовсвифиентерприсиапконфигуратион](../api/intune-deviceconfig-windowswifienterpriseeapconfiguration-delete.md)|Нет|Удаляет объект [виндовсвифиентерприсиапконфигуратион](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md).|
|[Обновление Виндовсвифиентерприсиапконфигуратион](../api/intune-deviceconfig-windowswifienterpriseeapconfiguration-update.md)|[виндовсвифиентерприсиапконфигуратион](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md)|Обновление свойств объекта [виндовсвифиентерприсиапконфигуратион](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md) .|

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Ключ объекта. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|lastModifiedDateTime|DateTimeOffset|Дата и время последнего изменения объекта. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|roleScopeTagIds|Коллекция строк|Список тегов областей для этого экземпляра сущности. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|суппортсскопетагс|Boolean|Указывает, поддерживает ли базовая конфигурация устройства назначение тегов области. Назначение свойства Скопетагс не разрешено, если это значение равно false, а сущности не будут отображаться для пользователей с ограниченной областью действия. Это происходит для устаревших политик, созданных в Silverlight, и может быть разрешено путем удаления и повторного создания политики на портале Azure. Это свойство доступно только для чтения. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|deviceManagementApplicabilityRuleOsEdition|[deviceManagementApplicabilityRuleOsEdition](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosedition.md)|Применимость выпусков ОС для этой политики. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|deviceManagementApplicabilityRuleOsVersion|[deviceManagementApplicabilityRuleOsVersion](../resources/intune-deviceconfig-devicemanagementapplicabilityruleosversion.md)|Правило применимости версии ОС для этой политики. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|deviceManagementApplicabilityRuleDeviceMode|[deviceManagementApplicabilityRuleDeviceMode](../resources/intune-deviceconfig-devicemanagementapplicabilityruledevicemode.md)|Правило применимости режима устройства для этой политики. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|createdDateTime|DateTimeOffset|Дата и время создания объекта. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|description|String|Указанное администратором описание конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|displayName|String|Указанное администратором имя конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|version|Int32|Версия конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|preSharedKey|String|Это предварительно общий ключ для сети WPA Personal Wi-Fi. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|вифисекурититипе|[вифисекурититипе](../resources/intune-deviceconfig-wifisecuritytype.md)|Укажите тип безопасности Wi-Fi. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md). Возможные значения: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.|
|метередконнектионлимит|[meteredConnectionLimitType](../resources/intune-deviceconfig-meteredconnectionlimittype.md)|Указать тип лимита межлимитного подключения для подключения WiFi. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md). Возможные значения: `unrestricted`, `fixed`, `variable`.|
|SSID|String|Укажите идентификатор SSID подключения WiFi. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|нетворкнаме|String|Укажите имя конфигурации сети. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|коннектаутоматикалли|Boolean|Указывает, должно ли подключение WiFi автоматически подключаться к сети в пределах диапазона. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|коннекттопреферреднетворк|Boolean|Укажите, должно ли подключение WiFi подключаться к более предпочтительным сетям, если оно уже подключено к этому.  Необходимо, чтобы Коннектаутоматикалли был true. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|коннектвхеннетворкнамеишидден|Boolean|Укажите, должно ли подключение WiFi автоматически подключаться, даже если идентификатор SSID не является широковещательным. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|проксисеттинг|[вифипроксисеттинг](../resources/intune-deviceconfig-wifiproxysetting.md)|Укажите параметры прокси-сервера для конфигурации Wi-Fi, унаследованной от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md). Возможные значения: `none`, `manual`, `automatic`.|
|проксимануаладдресс|String|Укажите IP-адрес прокси-сервера. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|проксимануалпорт|Int32|Укажите порт прокси-сервера. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|проксяутоматикконфигуратионурл|String|Укажите URL-адрес скрипта настройки прокси-сервера. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|форцефипскомплианце|Boolean|Укажите, следует ли применять соответствие требованиям FIPS. Наследуется от [виндовсвификонфигуратион](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|нетворксинглесигнон|[нетворксинглесигнонтипе](../resources/intune-deviceconfig-networksinglesignontype.md)|Укажите тип единого входа в сеть. Возможные значения: `disabled`, `prelogon`, `postlogon`.|
|максимумаусентикатионтимеаутинсекондс|Int32|Укажите максимальное время ожидания проверки подлинности (в секундах).  Допустимый диапазон: 1-120|
|усербаседвиртуаллан|Boolean|Укажите, следует ли изменить виртуальную локальную сеть, используемую устройством на основе учетных данных пользователя. Невозможно использовать, если для Нетворксинглесигнонтипе задано значение Disabled.|
|промптфораддитионалаусентикатионкредентиалс|Boolean|Укажите, должно ли подключение Wi-Fi запрашивать дополнительные учетные данные проверки подлинности.|
|енаблепаирвисемастеркэйкачинг|Boolean|Укажите, следует ли включить кэширование парных главных ключей в подключении Wi-Fi.|
|максимумпаирвисемастеркэйкачетимеинминутес|Int32|Указать максимальное время кэширования парных главных ключей (в минутах).  Допустимый диапазон: 5-1440|
|максимумнумберофпаирвисемастеркэйсинкаче|Int32|Укажите максимальное число парных главных ключей в кэше.  Допустимый диапазон: 1-255|
|енаблепреаусентикатион|Boolean|Укажите, следует ли включить предварительную проверку подлинности.|
|максимумпреаусентикатионаттемптс|Int32|Указать максимальное количество попыток перед проверкой подлинности.  Допустимый диапазон: 1-16|
|еаптипе|[еаптипе](../resources/intune-deviceconfig-eaptype.md)|Протокол расширенной проверки подлинности (EAP). Указывает тип протокола EAP, заданный для конечной точки Wi-Fi (маршрутизатора). Возможные значения: `eapTls`, `leap`, `eapSim`, `eapTtls`, `peap`, `eapFast`.|
|трустедсерверцертификатенамес|Коллекция строк|Укажите имена сертификатов доверенного сервера.|
|Параметр authenticationmethod|[вифиаусентикатионмесод](../resources/intune-deviceconfig-wifiauthenticationmethod.md)|Укажите метод проверки подлинности. Возможные значения: `certificate`, `usernameAndPassword`, `derivedCredential`.|
|Свойства innerauthenticationprotocolforeapttls|[нонеапаусентикатионмесодфореапттлстипе](../resources/intune-deviceconfig-noneapauthenticationmethodforeapttlstype.md)|Укажите внутренний протокол проверки подлинности для EAP TTLS. Возможные значения: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap`, `microsoftChapVersionTwo`.|
|outerIdentityPrivacyTemporaryValue|String|Укажите строку для замены имен пользователей для обеспечения конфиденциальности при использовании EAP TTLS или PEAP.|
|рекуирекриптографикбиндинг|Boolean|Указывает, следует ли включить криптографическую привязку при выборе типа EAP в качестве протокола PEAP.|
|перформсервервалидатион|Boolean|Укажите, следует ли включить проверку подлинности сервера путем проверки сертификата при выборе типа EAP в качестве PEAP.|
|дисаблеусерпромптфорсервервалидатион|Boolean|Укажите, следует ли запретить пользователю получать запросы на авторизацию новых серверов для доверенных центров сертификации, когда в качестве протокола PEAP выбран тип EAP.|
|аусентикатионпериодинсекондс|Int32|Укажите количество секунд, в течение которого клиент будет ждать после попытки проверки подлинности перед отказом. Допустимый диапазон 1-3600.|
|аусентикатионретриделайпериодинсекондс|Int32|Укажите количество секунд между неудачной проверкой подлинности и следующей попыткой проверки подлинности. Допустимый диапазон 1-3600.|
|еаполстартпериодинсекондс|Int32|Укажите время ожидания перед отправкой сообщения о запуске EAPOL (Extensible Authentication Protocol over LAN) в секундах. Допустимый диапазон 1-3600.|
|максимумеаполстартмессажес|Int32|Укажите максимальное число сообщений о запуске для отправки с помощью EAPOL (протокол расширенной проверки подлинности по локальной сети) перед возвращением отказа. Допустимый диапазон 1-100.|
|максимумаусентикатионфаилурес|Int32|Указывает максимальное количество сбоев проверки подлинности, разрешенных для набора учетных данных. Допустимый диапазон 1-100.|
|качекредентиалс|Boolean|Укажите, следует ли кэшировать учетные данные пользователя на устройстве, чтобы пользователям не нужно было вводить их каждый раз при каждом подключении.|
|authenticationType|[вифиаусентикатионтипе](../resources/intune-deviceconfig-wifiauthenticationtype.md)|Укажите, следует ли проверять подлинность пользователя, устройства, либо использовать гостевую проверку подлинности (None). Если вы используете проверку подлинности с помощью сертификата, убедитесь, что тип сертификата соответствует типу проверки подлинности. Возможные значения: `none`, `user`, `machine`, `machineOrUser`, `guest`.|

## <a name="relationships"></a>Связи
|Связь|Тип|Описание|
|:---|:---|:---|
|groupAssignments|Коллекция [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)|Список назначений групп для профиля конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|assignments|Коллекция [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|Список назначений для профиля конфигурации устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|deviceStatuses|Коллекция [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Состояние установки конфигурации для каждого устройства. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|userStatuses|Коллекция [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|Состояние установки конфигурации устройств пользователем. Наследуется от объекта [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|Обзор состояния конфигурации устройств. Наследуется от [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|Обзор состояния конфигурации устройств для пользователей. Наследуется от [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|deviceSettingStateSummaries|Коллекция [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Сводка данных о состоянии настройки конфигурации устройств. Наследуется от [deviceConfiguration](../resources/intune-shared-deviceconfiguration.md).|
|рутцертификатесфорсервервалидатион|Коллекция [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md)|Укажите корневой сертификат для проверки сервера.|
|идентитицертификатефорклиентаусентикатион|[windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)|Укажите сертификат удостоверения для проверки подлинности клиента.|
|рутцертификатефорклиентвалидатион|[windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md)|Укажите корневой сертификат для клиентской проверки.|

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsWifiEnterpriseEAPConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsWifiEnterpriseEAPConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "roleScopeTagIds": [
    "String"
  ],
  "supportsScopeTags": true,
  "deviceManagementApplicabilityRuleOsEdition": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsEdition",
    "osEditionTypes": [
      "String"
    ],
    "name": "String",
    "ruleType": "String"
  },
  "deviceManagementApplicabilityRuleOsVersion": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleOsVersion",
    "minOSVersion": "String",
    "maxOSVersion": "String",
    "name": "String",
    "ruleType": "String"
  },
  "deviceManagementApplicabilityRuleDeviceMode": {
    "@odata.type": "microsoft.graph.deviceManagementApplicabilityRuleDeviceMode",
    "deviceMode": "String",
    "name": "String",
    "ruleType": "String"
  },
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "preSharedKey": "String",
  "wifiSecurityType": "String",
  "meteredConnectionLimit": "String",
  "ssid": "String",
  "networkName": "String",
  "connectAutomatically": true,
  "connectToPreferredNetwork": true,
  "connectWhenNetworkNameIsHidden": true,
  "proxySetting": "String",
  "proxyManualAddress": "String",
  "proxyManualPort": 1024,
  "proxyAutomaticConfigurationUrl": "String",
  "forceFIPSCompliance": true,
  "networkSingleSignOn": "String",
  "maximumAuthenticationTimeoutInSeconds": 1024,
  "userBasedVirtualLan": true,
  "promptForAdditionalAuthenticationCredentials": true,
  "enablePairwiseMasterKeyCaching": true,
  "maximumPairwiseMasterKeyCacheTimeInMinutes": 1024,
  "maximumNumberOfPairwiseMasterKeysInCache": 1024,
  "enablePreAuthentication": true,
  "maximumPreAuthenticationAttempts": 1024,
  "eapType": "String",
  "trustedServerCertificateNames": [
    "String"
  ],
  "authenticationMethod": "String",
  "innerAuthenticationProtocolForEAPTTLS": "String",
  "outerIdentityPrivacyTemporaryValue": "String",
  "requireCryptographicBinding": true,
  "performServerValidation": true,
  "disableUserPromptForServerValidation": true,
  "authenticationPeriodInSeconds": 1024,
  "authenticationRetryDelayPeriodInSeconds": 1024,
  "eapolStartPeriodInSeconds": 1024,
  "maximumEAPOLStartMessages": 1024,
  "maximumAuthenticationFailures": 1024,
  "cacheCredentials": true,
  "authenticationType": "String"
}
```




