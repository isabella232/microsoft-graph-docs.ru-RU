---
title: Создание Граупполицимигратионрепорт
description: Создание нового объекта Граупполицимигратионрепорт.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 6e596370965334690712067728a54a396835ced3
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2019
ms.locfileid: "37535816"
---
# <a name="create-grouppolicymigrationreport"></a>Создание Граупполицимигратионрепорт

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Создание нового объекта [граупполицимигратионрепорт](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) .

## <a name="prerequisites"></a>Необходимые компоненты
Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

|Тип разрешения|Разрешения (в порядке убывания привилегий)|
|:---|:---|
|Делегированные (рабочая или учебная учетная запись)|DeviceManagementConfiguration.ReadWrite.All|
|Делегированные (личная учетная запись Майкрософт)|Не поддерживается.|
|Приложение|DeviceManagementConfiguration.ReadWrite.All|

## <a name="http-request"></a>HTTP-запрос
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/groupPolicyMigrationReports
```

## <a name="request-headers"></a>Заголовки запросов
|Заголовок|Значение|
|:---|:---|
|Авторизация|Bearer &lt;token&gt;. Обязательный.|
|Accept|application/json|

## <a name="request-body"></a>Текст запроса
В тексте запроса добавьте представление объекта Граупполицимигратионрепорт в формате JSON.

В следующей таблице приведены свойства, необходимые при создании Граупполицимигратионрепорт.

|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Пока не задокументировано.|
|граупполициобжектид|GUID|GUID объекта групповой политики из XML-содержимого объекта групповой политики|
|displayName|Строка|Имя объекта групповой политики из XML-содержимого объекта групповой политики|
|аудистингуишеднаме|String|Различающееся имя подразделения.|
|createdDateTime|DateTimeOffset|Дата и время создания Граупполицимигратионрепорт.|
|lastModifiedDateTime|DateTimeOffset|Дата и время последнего изменения Граупполицимигратионрепорт.|
|граупполицикреатеддатетиме|DateTimeOffset|Дата и время создания Граупполицимигратионрепорт.|
|граупполициластмодифиеддатетиме|DateTimeOffset|Дата и время последнего изменения Граупполицимигратионрепорт.|
|мигратионреадинесс|[граупполицимигратионреадинесс](../resources/intune-gpanalyticsservice-grouppolicymigrationreadiness.md)|Область действия Intune для связанного файлового объекта групповой политики. Возможные значения: `none`, `partial`, `complete`, `error`, `notApplicable`.|
|таржетединактиведиректори|Логический|Свойство Targeted в Active Directory из XML-контента объекта групповой политики|
|тоталсеттингскаунт|Int32|Общее количество параметров групповой политики из файла GPO.|
|суппортедсеттингскаунт|Int32|Количество параметров групповой политики, поддерживаемых Intune.|
|суппортедсеттингсперцент|Int32|Процент параметров групповой политики, поддерживаемых Intune.|



## <a name="response"></a>Отклик
В случае успешного выполнения этот метод возвращает `201 Created` код отклика и объект [граупполицимигратионрепорт](../resources/intune-gpanalyticsservice-grouppolicymigrationreport.md) в тексте отклика.

## <a name="example"></a>Пример

### <a name="request"></a>Запрос
Ниже приведен пример запроса.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/groupPolicyMigrationReports
Content-type: application/json
Content-length: 544

{
  "@odata.type": "#microsoft.graph.groupPolicyMigrationReport",
  "groupPolicyObjectId": "ca1c97af-97af-ca1c-af97-1ccaaf971cca",
  "displayName": "Display Name value",
  "ouDistinguishedName": "Ou Distinguished Name value",
  "groupPolicyCreatedDateTime": "2016-12-31T23:58:14.0676812-08:00",
  "groupPolicyLastModifiedDateTime": "2017-01-01T00:02:51.2241017-08:00",
  "migrationReadiness": "partial",
  "targetedInActiveDirectory": true,
  "totalSettingsCount": 2,
  "supportedSettingsCount": 6,
  "supportedSettingsPercent": 8
}
```

### <a name="response"></a>Отклик
Ниже приведен пример ответа. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 716

{
  "@odata.type": "#microsoft.graph.groupPolicyMigrationReport",
  "id": "60663fa8-3fa8-6066-a83f-6660a83f6660",
  "groupPolicyObjectId": "ca1c97af-97af-ca1c-af97-1ccaaf971cca",
  "displayName": "Display Name value",
  "ouDistinguishedName": "Ou Distinguished Name value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "groupPolicyCreatedDateTime": "2016-12-31T23:58:14.0676812-08:00",
  "groupPolicyLastModifiedDateTime": "2017-01-01T00:02:51.2241017-08:00",
  "migrationReadiness": "partial",
  "targetedInActiveDirectory": true,
  "totalSettingsCount": 2,
  "supportedSettingsCount": 6,
  "supportedSettingsPercent": 8
}
```





